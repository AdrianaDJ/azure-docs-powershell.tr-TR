---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106200"
---
# <span data-ttu-id="945cf-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="945cf-101">New-AzureVM</span></span>

## <span data-ttu-id="945cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="945cf-102">SYNOPSIS</span></span>
<span data-ttu-id="945cf-103">Azure sanal makinesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="945cf-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="945cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="945cf-104">SYNTAX</span></span>

### <span data-ttu-id="945cf-105">ExistingService (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="945cf-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="945cf-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="945cf-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="945cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="945cf-107">DESCRIPTION</span></span>
<span data-ttu-id="945cf-108">**New-AzureVM** cmdlet 'i var olan bir Azure hizmetine yeni bir sanal makine ekler ya da *Location* veya *affinitygroup* belirtilmişse geçerli abonelikte sanal makine ve hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="945cf-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="945cf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="945cf-109">EXAMPLES</span></span>

### <span data-ttu-id="945cf-110">Örnek 1: Windows yapılandırması için sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="945cf-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="945cf-111">Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve belirtilen benzeşim grubunda sanal makine oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="945cf-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="945cf-112">Örnek 2: Linux yapılandırması için sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="945cf-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="945cf-113">Bu komut, Linux için sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve belirtilen benzeşim grubunda sanal makine oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="945cf-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="945cf-114">Örnek 3: sanal makine oluşturma ve veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="945cf-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="945cf-115">İlk iki komut **Get-AzureVMImage** cmdlet 'ini kullanarak kullanılabilir resimleri alır ve bunlardan birini $Image değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="945cf-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="945cf-116">Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve Azure veri disketiyle sanal makine oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="945cf-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="945cf-117">Örnek 4: ayrılmış IP adresine sahip sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="945cf-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="945cf-118">Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve ayrılmış IP adresi içeren bir sanal makine oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="945cf-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="945cf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="945cf-119">PARAMETERS</span></span>

### <span data-ttu-id="945cf-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="945cf-120">-AffinityGroup</span></span>
<span data-ttu-id="945cf-121">Bulut hizmetinin bulunduğu Azure benzeşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="945cf-122">Bu parametre yalnızca bu cmdlet bir bulut hizmeti oluşturduğunda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="945cf-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="945cf-123">-DeploymentLabel</span></span>
<span data-ttu-id="945cf-124">Dağıtım için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-124">Specifies a label for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="945cf-125">-DeploymentName</span></span>
<span data-ttu-id="945cf-126">Dağıtım adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-126">Specifies a deployment name.</span></span>
<span data-ttu-id="945cf-127">Belirtilmemişse, bu cmdlet dağıtım adı olarak hizmet adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="945cf-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="945cf-128">-DnsSettings</span></span>
<span data-ttu-id="945cf-129">Yeni dağıtımın DNS ayarlarını tanımlayan bir DNS sunucusu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="945cf-130">-InformationAction</span></span>
<span data-ttu-id="945cf-131">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="945cf-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="945cf-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="945cf-133">'A</span><span class="sxs-lookup"><span data-stu-id="945cf-133">Continue</span></span>
- <span data-ttu-id="945cf-134">Manıza</span><span class="sxs-lookup"><span data-stu-id="945cf-134">Ignore</span></span>
- <span data-ttu-id="945cf-135">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="945cf-135">Inquire</span></span>
- <span data-ttu-id="945cf-136">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="945cf-136">SilentlyContinue</span></span>
- <span data-ttu-id="945cf-137">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="945cf-137">Stop</span></span>
- <span data-ttu-id="945cf-138">Biliriz</span><span class="sxs-lookup"><span data-stu-id="945cf-138">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-139">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="945cf-139">-InformationVariable</span></span>
<span data-ttu-id="945cf-140">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-140">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-141">-Internalloadbalancerconfig</span><span class="sxs-lookup"><span data-stu-id="945cf-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="945cf-142">Dahili bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="945cf-143">Bu parametre kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="945cf-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-144">-Konum</span><span class="sxs-lookup"><span data-stu-id="945cf-144">-Location</span></span>
<span data-ttu-id="945cf-145">Yeni hizmeti barındıran konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="945cf-146">Hizmet zaten varsa, bu parametreyi belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="945cf-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="945cf-147">-Profile</span></span>
<span data-ttu-id="945cf-148">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="945cf-149">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="945cf-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-150">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="945cf-150">-ReservedIPName</span></span>
<span data-ttu-id="945cf-151">Ayrılmış IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-151">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-152">-Smardnsfqdn</span><span class="sxs-lookup"><span data-stu-id="945cf-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="945cf-153">Geriye doğru DNS için tam etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="945cf-154">-ServiceDescription</span></span>
<span data-ttu-id="945cf-155">Yeni hizmetin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="945cf-156">-ServiceLabel</span></span>
<span data-ttu-id="945cf-157">Yeni hizmet için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-158">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="945cf-158">-ServiceName</span></span>
<span data-ttu-id="945cf-159">Yeni veya var olan hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="945cf-160">Hizmet yoksa, bu cmdlet sizin için oluşturur.</span><span class="sxs-lookup"><span data-stu-id="945cf-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="945cf-161">Servisin oluşturulacağı yeri belirtmek için *Location* veya *affinitygroup* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="945cf-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="945cf-162">Hizmet varsa, *Location* veya *affinitygroup* parametresi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="945cf-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-163">-VM 'Ler</span><span class="sxs-lookup"><span data-stu-id="945cf-163">-VMs</span></span>
<span data-ttu-id="945cf-164">Oluşturulacak sanal makine nesnelerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-165">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="945cf-165">-VNetName</span></span>
<span data-ttu-id="945cf-166">Bu cmdlet 'in sanal makineyi dağıttığı sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="945cf-167">-WaitForBoot</span></span>
<span data-ttu-id="945cf-168">Bu cmdlet 'in sanal makinenin **Readyrole** durumuna ulaşmasını beklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="945cf-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="945cf-169">Bu cmdlet beklenirken, sanal makine şu durumlardan birine gelirse başarısız olur: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="945cf-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945cf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945cf-170">CommonParameters</span></span>
<span data-ttu-id="945cf-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="945cf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945cf-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945cf-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945cf-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="945cf-173">INPUTS</span></span>

## <span data-ttu-id="945cf-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="945cf-174">OUTPUTS</span></span>

## <span data-ttu-id="945cf-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="945cf-175">NOTES</span></span>

## <span data-ttu-id="945cf-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="945cf-176">RELATED LINKS</span></span>

[<span data-ttu-id="945cf-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="945cf-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="945cf-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="945cf-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="945cf-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="945cf-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="945cf-180">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="945cf-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


