---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591717"
---
# <span data-ttu-id="f15ae-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f15ae-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="f15ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f15ae-103">VMSUBNET 'e bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f15ae-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f15ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f15ae-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f15ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f15ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f15ae-106">**Add-Azurermvmssdiagnosticsextencmdlet** 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f15ae-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f15ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f15ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f15ae-108">Örnek 1: VMSS 'ye tanılama uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f15ae-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="f15ae-109">Bu komut, VMSS 'ye bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f15ae-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="f15ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f15ae-110">PARAMETERS</span></span>

### <span data-ttu-id="f15ae-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f15ae-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f15ae-112">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f15ae-113">-Force</span></span>
<span data-ttu-id="f15ae-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f15ae-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f15ae-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f15ae-115">-Name</span></span>
<span data-ttu-id="f15ae-116">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-117">-Protectedsettingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="f15ae-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="f15ae-118">Özel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-118">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="f15ae-119">-Settingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="f15ae-119">-SettingFilePath</span></span>
<span data-ttu-id="f15ae-120">Genel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f15ae-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="f15ae-122">Bu VMSS için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="f15ae-123">Sürümü edinmek için, [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'Ini *PublisherName* parametresi ve *tür* parametresi için ıaasdiagnostics değeriyle çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f15ae-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f15ae-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f15ae-125">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f15ae-125">Specify the VMSS object.</span></span>
<span data-ttu-id="f15ae-126">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f15ae-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f15ae-127">-Confirm</span></span>
<span data-ttu-id="f15ae-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f15ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15ae-129">-WhatIf</span></span>
<span data-ttu-id="f15ae-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f15ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15ae-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f15ae-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15ae-132">CommonParameters</span></span>
<span data-ttu-id="f15ae-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f15ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15ae-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15ae-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15ae-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f15ae-135">INPUTS</span></span>

### <span data-ttu-id="f15ae-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f15ae-136">None</span></span>
<span data-ttu-id="f15ae-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f15ae-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f15ae-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f15ae-138">OUTPUTS</span></span>

###  
<span data-ttu-id="f15ae-139">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f15ae-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f15ae-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f15ae-140">NOTES</span></span>

## <span data-ttu-id="f15ae-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f15ae-141">RELATED LINKS</span></span>

[<span data-ttu-id="f15ae-142">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="f15ae-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="f15ae-143">Remove-azurermvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="f15ae-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="f15ae-144">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="f15ae-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
