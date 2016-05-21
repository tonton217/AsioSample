import os

env = Environment()
boost_prefix = "/usr/local"
sync_timer_src = env.Glob("src/sync_timer/*.cc")
async_timer_src = env.Glob("src/async_timer/*.cc")
env.Append(CPPPATH = [os.path.join(boost_prefix, "include")])
env.Append(LIBPATH = [os.path.join(boost_prefix, "lib")])
sync_timer = env.Program(target = "bin/sync_timer", source = sync_timer_src, LIBS = ['boost_system-mt', 'boost_regex-mt'])
async_timer = env.Program(target = "bin/async_timer", source = async_timer_src, LIBS = ['boost_system-mt', 'boost_regex-mt', 'boost_thread-mt'])

env.Default(sync_timer)
env.Default(async_timer)

