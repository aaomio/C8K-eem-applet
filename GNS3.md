# GNS3 Setup

This guide covers setting up **GNS3 with the GNS3 VM in VMware Workstation** and adding a **Cisco Catalyst 8000V (C8KV)** image for IOS XE labs.

## Requirements

* VMware Workstation
* GNS3
* GNS3 VM
* Cisco Catalyst 8000V IOS XE image

---

# 1. Install GNS3

Download and install GNS3 for Windows:

[GNS3 Downloads](https://www.gns3.com/software/download)

The GNS3 Windows installer provides the GNS3 desktop application.

---

# 2. Download the GNS3 VM

The GNS3 VM is distributed by GNS3 as an archive containing the virtual machine.

[GNS3 VM Downloads](https://www.gns3.com/software/download)

Download the **VMware Workstation** version.

The downloaded archive will contain a file similar to:

```text
GNS3 VM.ova
```

---

# 3. Import `GNS3 VM.ova` into VMware Workstation

Extract the downloaded GNS3 VM archive.

The extracted directory should contain:

```text
GNS3 VM.ova
```

Open **VMware Workstation**.

Select:

```text
File
    > Open
```

Browse to:

```text
GNS3 VM.ova
```

Select the OVA and open it.

VMware will display the import dialog.

Keep the VM name as:

```text
GNS3 VM
```

Choose the location where the virtual machine should be stored and select **Import**.


---

# 4. Configure VMware Virtualisation

Before starting the GNS3 VM, open:

```text
GNS3 VM
    > Settings
    > Processors
```

Enable:

```text
Virtualize Intel VT-x/EPT
```

or the equivalent AMD virtualisation option.

This allows the GNS3 VM to use hardware virtualisation for its QEMU appliances.

---

# 5. Start the GNS3 VM

Start:

```text
GNS3 VM
```

The VM will boot into the GNS3 VM environment.

The console should display information about the GNS3 server and its IP address.

For example:

```text
GNS3 server version: 2.x
IP: 192.168.x.x
```

The exact IP address will depend on the VMware network configuration.

---

# 6. Connect GNS3 to the GNS3 VM

Open GNS3.

Go to:

```text
Edit
    > Preferences
        > GNS3 VM
```

Enable:

```text
Enable the GNS3 VM
```

Select:

```text
VMware Workstation
```

Select the imported:

```text
GNS3 VM
```

Click:

```text
Apply
OK
```

The GNS3 VM should now be available to GNS3.

The GNS3 documentation provides the GNS3 VM integration process for VMware.

---


