---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937080"
---
# <span data-ttu-id="0f225-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f225-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="0f225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f225-102">SYNOPSIS</span></span>
<span data-ttu-id="0f225-103">VMSUBNET 'e bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f225-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="0f225-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f225-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f225-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f225-105">DESCRIPTION</span></span>
<span data-ttu-id="0f225-106">**Add-Azvmssdiagnosticsextenma** cmdlet 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f225-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0f225-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f225-107">EXAMPLES</span></span>

### <span data-ttu-id="0f225-108">Örnek 1: VMSS 'ye tanılama uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f225-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="0f225-109">Bu komut, VMSS 'ye bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f225-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="0f225-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f225-110">PARAMETERS</span></span>

### <span data-ttu-id="0f225-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0f225-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0f225-112">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f225-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="0f225-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f225-113">-DefaultProfile</span></span>
<span data-ttu-id="0f225-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f225-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f225-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0f225-115">-Force</span></span>
<span data-ttu-id="0f225-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0f225-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f225-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f225-117">-Name</span></span>
<span data-ttu-id="0f225-118">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f225-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="0f225-119">-Protectedsettingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="0f225-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="0f225-120">Özel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f225-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="0f225-121">-Settingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="0f225-121">-SettingFilePath</span></span>
<span data-ttu-id="0f225-122">Genel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f225-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="0f225-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0f225-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="0f225-124">Bu VMSS için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f225-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="0f225-125">Sürümü edinmek için, *PublisherName* parametresi ve *tür* parametresi için ıaasdiagnostics değeriyle [Get-azvmextensionımage](./Get-AzVMExtensionImage.md) cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="0f225-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="0f225-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f225-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0f225-127">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0f225-127">Specify the VMSS object.</span></span>
<span data-ttu-id="0f225-128">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f225-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0f225-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f225-129">-Confirm</span></span>
<span data-ttu-id="0f225-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f225-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f225-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f225-131">-WhatIf</span></span>
<span data-ttu-id="0f225-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f225-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f225-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f225-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f225-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f225-134">CommonParameters</span></span>
<span data-ttu-id="0f225-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f225-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f225-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f225-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f225-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f225-137">INPUTS</span></span>

### <span data-ttu-id="0f225-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f225-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="0f225-139">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0f225-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="0f225-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f225-140">OUTPUTS</span></span>

###  
<span data-ttu-id="0f225-141">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0f225-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0f225-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f225-142">NOTES</span></span>

## <span data-ttu-id="0f225-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f225-143">RELATED LINKS</span></span>

[<span data-ttu-id="0f225-144">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0f225-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="0f225-145">Remove-azvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="0f225-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="0f225-146">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="0f225-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
