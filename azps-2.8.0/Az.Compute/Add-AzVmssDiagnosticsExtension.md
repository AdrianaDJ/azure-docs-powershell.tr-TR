---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 55abb45cb689f05f721ed42afadb855638f90256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752989"
---
# <span data-ttu-id="6fae3-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6fae3-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="6fae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fae3-102">SYNOPSIS</span></span>
<span data-ttu-id="6fae3-103">VMSUBNET 'e bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="6fae3-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="6fae3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fae3-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fae3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fae3-105">DESCRIPTION</span></span>
<span data-ttu-id="6fae3-106">**Add-Azvmssdiagnosticsextenma** cmdlet 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="6fae3-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6fae3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fae3-107">EXAMPLES</span></span>

### <span data-ttu-id="6fae3-108">Örnek 1: VMSS 'ye tanılama uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="6fae3-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="6fae3-109">Bu komut, VMSS 'ye bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="6fae3-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="6fae3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fae3-110">PARAMETERS</span></span>

### <span data-ttu-id="6fae3-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6fae3-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6fae3-112">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fae3-113">-DefaultProfile</span></span>
<span data-ttu-id="6fae3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fae3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fae3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6fae3-115">-Force</span></span>
<span data-ttu-id="6fae3-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6fae3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fae3-117">-Name</span></span>
<span data-ttu-id="6fae3-118">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-119">-Protectedsettingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="6fae3-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="6fae3-120">Özel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-121">-Settingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="6fae3-121">-SettingFilePath</span></span>
<span data-ttu-id="6fae3-122">Genel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6fae3-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="6fae3-124">Bu VMSS için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="6fae3-125">Sürümü edinmek için, *PublisherName* parametresi ve *tür* parametresi için ıaasdiagnostics değeriyle [Get-azvmextensionımage](./Get-AzVMExtensionImage.md) cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6fae3-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6fae3-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6fae3-127">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6fae3-127">Specify the VMSS object.</span></span>
<span data-ttu-id="6fae3-128">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fae3-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fae3-129">-Confirm</span></span>
<span data-ttu-id="6fae3-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fae3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fae3-131">-WhatIf</span></span>
<span data-ttu-id="6fae3-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fae3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fae3-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fae3-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fae3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fae3-134">CommonParameters</span></span>
<span data-ttu-id="6fae3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fae3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fae3-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fae3-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fae3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fae3-137">INPUTS</span></span>

### <span data-ttu-id="6fae3-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6fae3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6fae3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6fae3-139">System.String</span></span>

### <span data-ttu-id="6fae3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fae3-140">System.Boolean</span></span>

## <span data-ttu-id="6fae3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fae3-141">OUTPUTS</span></span>

### <span data-ttu-id="6fae3-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6fae3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6fae3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fae3-143">NOTES</span></span>

## <span data-ttu-id="6fae3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fae3-144">RELATED LINKS</span></span>

[<span data-ttu-id="6fae3-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6fae3-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="6fae3-146">Remove-azvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="6fae3-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="6fae3-147">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="6fae3-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)