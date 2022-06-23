# CKA-Exam-Experienced-Sharing

Hello Kubernetes guys...

Nice to see you virtually. Are you looking for Kubernetes Exams Review? If yes, you are in the right place. Let's start on my experience of the CKA exam. BTW, if you want to know the experience about CKAD, here is the CKAD Exam Review (https://github.com/thawzinmyo/CKAD-Exam-Experienced-Sharing).

I have been certified with CKAD last 3 months. So, in my mind theory and concepts, related to Kubernetes are still fresh. 

## Learning resources ##

Firstly, I study CKA with Mumshad Mammanbeth's course and practice it. I want to mention again that [Mumshad's](https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests/) course is great in presentation. If you study with another good teacher, you are also in right place. Whatever you learn from whom, well understanding is the important thing. And I have some experience or challenges with Kubernetes. That is [CKA-Challange](https://github.com/thawzinmyo/The-Hackathon-Challenge-DevOps) held by KodeKloud last May,2022. I participated in that challenge. And I won the CKA Exam Voucher. So now, that exam is sponsored by KodeKloud, you can say that. Thank you so much for that, KodeKloud Team. 

In the Challenge, I was tested Deployment, Image Security with trivy and AppAmor, Persistent Volume, Persistent Volume Claim, Network Policies and api pod health and its service ( my favorite ones ), etc.
So, I got some hands-on experience with that and I am also a member of KodeKloud Engineer, now tasks are postponed in DevOps Architect Role, still exciting to practice it.

## Self-Studying vs Work ##

After I studied and sit CKAD exam, I got a new job. Studying at work is not quick before being jobless. Because Work is more important than private study. So, I studied for 1 hour per day for CKA.
I hope that you already know that feeling. So, if you are working, prepare for time management between Work and Private Study. 

While I sit CKAD, I already mentioned my excitement during the exam. At that time, I am not feeling like that before experience. My mind is cool and relaxed. 

## Prepare Exam Environment ##
So, you should schedule the exam when the Internet and Electric are stable situations in Myanmar. One thing has happened that before the exam within 30 Min, the electricity is cut off. I am so worried because my laptop battery can't stand for 2 hours. 
Actually, the exam is 2 hours but you will expect 30 min for Check-In time, the proctor will ask some questions and you need to show your ID card( Passport, or Visa Card, or National ID). After you passed check-in, you will need to start your exam!

### So, during the exam ... ###

 - Verify that you switched the correct context. If you didn't switch the correct context (given), you will get zero! Verify!!! Verify !!! Verify!!!
 - Time management is key. So, try to use imperative commands as possible as
 - Don't panic when you are stuck on some questions. Flag it and come back when you know some insightful idea
 - Don't hurry up in reading questions! Need to create namespace or not?, need to add env?, labels? Always verify your results after you create or deploy something!
 - Try to use Vim or Vi editor as a professional (practice daily usage before exam)
 - Bookmark useful official Kubernetes Document in the web browser (During the exam, I can't forward Docker official site! The proctor didn't allow me!)
 - Spend more time with Kubernetes Documents ( kubernetes.io/docs/ ). There are many solutions for you.


### Example Scenarios ###

 - First, create PV and PVC and add that PVC as the volume in Pod then modify the storage request 
 - Network Policy (Pods from the "DB" namespace can only accept pods under the "frontend" namespace.
 - Create ServiceAccount under namespace and give a permit to that ServiceAccount using Role, Rolebinding, ClusterRole, ClusterRolebinding
 - Create Multi Container, Sidecar pattern, Scale that Deployment and expose service as NodePort Service Type
 - Practice querying from JSON format
 - Practice to schedule pods to specific Node
 - Practice Cluster Upgrade, ETCD Backup, and Restore
 - Taint and Toleration, Node Affinity and anti-Affinity 
 - Practice monitoring Pods and Nodes that request resources

## Example imperative commands and userful commands ##

`run pod temporarily`
<details>
<summary> Command </summary>
<p>

```bash
 $ kubernetes run test-pod --image nginx -it --rm --restart=Never -- curl <IP>:<PORT>
```

</p>
</details>

---

`create Ingress`
<details>
<summary> Command </summary>
<p>

```bash
 $ kubectl create ingress my-ingress --rule=/path=my-service:8080
```
</p>
</details>

---

`expose service using pod label`
<details>
<summary> Command </summary>
<p>

```bash
$ kubectl run nginx --image nginx --port --expose
```
</p>
</details>

---

`inspect certificate`

<details>
<summary> Command </summary>
<p>

```bash
 $ openssl x509 -noout -text -in /etc/kubernetes/pki/apiserver.crt
 ```
</p>
</details>

---

`print out as one line`
<details>
<summary> Command </summary>
<p>

```bash
 $ cat example.cert | base64 -w 0 (it will output as oneline)
```
</p>
</details>

---

`inspecting kubelet service using journalctl`
<details>
<summary> Command </summary>
<p>

```bash
 $ journalctl -u kubelet | grep -i kubelet
```
</p>
</details>

---

`query kubelet process`

<details>
<summary> Command </summary>
<p>

```bash
 $ ps -aux | grep -i kubelet
```
</p>
</details>

---

`prepare vimrc for manifest file`

```bash
$ vi ~/.vimrc
```
```bash
set expandtab
set tabstop=2
set shiftwidth=2
```
All of these command will help you when you sit the exam. 

I don't even use many aliases. Exam Environment will set with auto-completion. It's so useful and thanks for that.
I sit the exam with mobile Internet and cost 1 GB for two and half hours. Need to verify your mobile Internet. (Sitting exam with mobile internet may be a risk.) You need to take that risk. I will share with you some screenshots of my exam room and mobile internet traffic monitor. I got 20 min to review during the exam. It's different from the previous CKAD exam. With CKAD, I don't have enough time.

All of these are my experience on CKA.  I hope that my experience will help you. If you have any questions about CKA and CKAD, please contact me on any social platform. Good luck with your exam! Believe yourself! 

"Everyone can cook"  

Make a coffee for my journey https://www.buymeacoffee.com/thawzinmyo 😜
