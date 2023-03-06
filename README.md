# reader-writer
we have used 3 semaphore(mutex,rw,write) and a variable r_c.
rw is common to both the section

Reader Part will wait until writer procces complete it execution and release wr variable.
then it will check mutex variabe which is used to check wheather another reader is trying to change readcount variable.

in this reader part the very first reader will set wrt to 0 which will stop other writers to enter the writer section but if writer tries to enter into the critical section it will set rw
to 0 which will stop other readers to enter into the reader section.

as rw will become 0 , all the reader which are into the critical section will complete their execution then the writer will get to enter the section ,while writer is inside the critical section all other readers and writers have to wait for their section.

in this way this code will work as starve free reader writer.
