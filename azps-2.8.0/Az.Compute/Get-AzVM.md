---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 5fd3e89a20dba274c1bdcad69bed150e9d20fc22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752936"
---
# <span data-ttu-id="39666-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-101">Get-AzVM</span></span>

## <span data-ttu-id="39666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39666-102">SYNOPSIS</span></span>
<span data-ttu-id="39666-103">Sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="39666-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="39666-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39666-104">SYNTAX</span></span>

### <span data-ttu-id="39666-105">DefaultParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39666-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39666-106">Getvirtualmachineınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="39666-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39666-107">Listlocationvirtual</span><span class="sxs-lookup"><span data-stu-id="39666-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39666-108">Listnextlinkvirtual, Inesparamset</span><span class="sxs-lookup"><span data-stu-id="39666-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39666-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="39666-109">DESCRIPTION</span></span>
<span data-ttu-id="39666-110">**Get-azıvm** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="39666-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="39666-111">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="39666-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="39666-112">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="39666-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="39666-113">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="39666-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="39666-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39666-114">EXAMPLES</span></span>

### <span data-ttu-id="39666-115">Örnek 1: model ve örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="39666-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="39666-116">Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="39666-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="39666-117">Örnek 2: örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="39666-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="39666-118">Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="39666-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="39666-119">Bu komut, *Status* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="39666-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="39666-120">Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="39666-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="39666-121">Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="39666-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="39666-122">Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="39666-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="39666-123">Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="39666-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="39666-124">Bu komut aboneliğinizdeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="39666-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="39666-125">Örnek 5: konumdaki tüm sanal makineleri edinin.</span><span class="sxs-lookup"><span data-stu-id="39666-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="39666-126">Bu komut, Batı ABD bölgesindeki tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="39666-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="39666-127">Örnek 6: filtreleme kullanarak tüm sanal makineleri alma</span><span class="sxs-lookup"><span data-stu-id="39666-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="39666-128">Bu komut aboneliğinizdeki "test" ile başlayan tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="39666-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="39666-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39666-129">PARAMETERS</span></span>

### <span data-ttu-id="39666-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39666-130">-DefaultProfile</span></span>
<span data-ttu-id="39666-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39666-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39666-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="39666-132">-DisplayHint</span></span>
<span data-ttu-id="39666-133">Sanal makine nesnesinin nasıl görüntülendiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="39666-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="39666-134">Geçerli değerler:--Compact: yalnızca üst düzey özelliklerini görüntüler--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler</span><span class="sxs-lookup"><span data-stu-id="39666-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39666-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="39666-135">-Location</span></span>
<span data-ttu-id="39666-136">Görüntülenecek sanal makinelerin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="39666-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39666-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="39666-137">-Name</span></span>
<span data-ttu-id="39666-138">Alınacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39666-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="39666-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="39666-139">-NextLink</span></span>
<span data-ttu-id="39666-140">Sonraki bağlantıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="39666-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39666-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39666-141">-ResourceGroupName</span></span>
<span data-ttu-id="39666-142">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39666-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="39666-143">-Durum</span><span class="sxs-lookup"><span data-stu-id="39666-143">-Status</span></span>
<span data-ttu-id="39666-144">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39666-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39666-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39666-145">CommonParameters</span></span>
<span data-ttu-id="39666-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39666-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39666-147">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39666-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39666-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39666-148">INPUTS</span></span>

### <span data-ttu-id="39666-149">System. String</span><span class="sxs-lookup"><span data-stu-id="39666-149">System.String</span></span>

### <span data-ttu-id="39666-150">System. Uri</span><span class="sxs-lookup"><span data-stu-id="39666-150">System.Uri</span></span>

### <span data-ttu-id="39666-151">Microsoft. Azure. Commands. COMPUTE. modeller. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="39666-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="39666-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39666-152">OUTPUTS</span></span>

### <span data-ttu-id="39666-153">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39666-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="39666-154">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="39666-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="39666-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39666-155">NOTES</span></span>

## <span data-ttu-id="39666-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39666-156">RELATED LINKS</span></span>

[<span data-ttu-id="39666-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="39666-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="39666-159">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="39666-160">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="39666-161">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="39666-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="39666-162">Update-AzVM</span></span>](./Update-AzVM.md)

