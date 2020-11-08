---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106038"
---
# <span data-ttu-id="fe65a-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe65a-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="fe65a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe65a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe65a-103">Sanal makinede Azure tanılama uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="fe65a-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="fe65a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe65a-104">SYNTAX</span></span>

### <span data-ttu-id="fe65a-105">Setdiagnosticsextenma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe65a-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fe65a-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="fe65a-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe65a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65a-107">DESCRIPTION</span></span>
<span data-ttu-id="fe65a-108">**Set-AzureVMDiagnosticsExtension** cmdlet 'i, bir sanal makinede Microsoft Azure tanılama uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="fe65a-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="fe65a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe65a-109">EXAMPLES</span></span>

### <span data-ttu-id="fe65a-110">Örnek 1: Azure tanılama uzantısı uygulanmış sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe65a-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="fe65a-111">Bu komutlar, bir sanal makinede Azure tanılama uzantısını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="fe65a-112">Örnek 2: var olan bir sanal makinede Azure tanılama uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fe65a-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="fe65a-113">İlk komut, bir sanal makine almak için **Get-AzureVM** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fe65a-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="fe65a-114">İkinci komut, sanal makine yapılandırmasını Azure Diagnostics uzantısını içerecek şekilde güncelleştirmek için **set-AzureVMDiagnosticsExtension** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fe65a-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="fe65a-115">Son komutu, güncelleştirilmiş yapılandırmayı sanal makineye uygular.</span><span class="sxs-lookup"><span data-stu-id="fe65a-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="fe65a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe65a-116">PARAMETERS</span></span>

### <span data-ttu-id="fe65a-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="fe65a-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="fe65a-118">Tanılama yapılandırması için bir yol belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-119">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="fe65a-119">-Disable</span></span>
<span data-ttu-id="fe65a-120">Bu cmdlet 'in sanal makinedeki tanılama uzantısını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fe65a-121">-InformationAction</span></span>
<span data-ttu-id="fe65a-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe65a-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe65a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe65a-124">'A</span><span class="sxs-lookup"><span data-stu-id="fe65a-124">Continue</span></span>
- <span data-ttu-id="fe65a-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="fe65a-125">Ignore</span></span>
- <span data-ttu-id="fe65a-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fe65a-126">Inquire</span></span>
- <span data-ttu-id="fe65a-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fe65a-127">SilentlyContinue</span></span>
- <span data-ttu-id="fe65a-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fe65a-128">Stop</span></span>
- <span data-ttu-id="fe65a-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fe65a-129">Suspend</span></span>

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

### <span data-ttu-id="fe65a-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fe65a-130">-InformationVariable</span></span>
<span data-ttu-id="fe65a-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe65a-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe65a-132">-Profile</span></span>
<span data-ttu-id="fe65a-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe65a-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fe65a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe65a-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="fe65a-135">-ReferenceName</span></span>
<span data-ttu-id="fe65a-136">Tanılama uzantısının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe65a-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="fe65a-138">Bir depolama hesabı uç noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe65a-139">-StorageAccountKey</span></span>
<span data-ttu-id="fe65a-140">Bir depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fe65a-141">-StorageAccountName</span></span>
<span data-ttu-id="fe65a-142">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fe65a-143">-StorageContext</span></span>
<span data-ttu-id="fe65a-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-145">-Version</span><span class="sxs-lookup"><span data-stu-id="fe65a-145">-Version</span></span>
<span data-ttu-id="fe65a-146">Uzantı sürümünü dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-147">-VM</span><span class="sxs-lookup"><span data-stu-id="fe65a-147">-VM</span></span>
<span data-ttu-id="fe65a-148">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe65a-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe65a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe65a-149">CommonParameters</span></span>
<span data-ttu-id="fe65a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe65a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe65a-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe65a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe65a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe65a-152">INPUTS</span></span>

## <span data-ttu-id="fe65a-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe65a-153">OUTPUTS</span></span>

## <span data-ttu-id="fe65a-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe65a-154">NOTES</span></span>

## <span data-ttu-id="fe65a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe65a-155">RELATED LINKS</span></span>

[<span data-ttu-id="fe65a-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe65a-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fe65a-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe65a-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fe65a-158">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fe65a-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


