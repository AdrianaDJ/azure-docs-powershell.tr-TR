---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4370a7b87ee87b223ddadd6f872b549c2537e1e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591370"
---
# <span data-ttu-id="afe71-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="afe71-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="afe71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe71-102">SYNOPSIS</span></span>
<span data-ttu-id="afe71-103">VMSUBNET 'e bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="afe71-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afe71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afe71-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afe71-105">DESCRIPTION</span></span>
<span data-ttu-id="afe71-106">**Add-Azurermvmssdiagnosticsextencmdlet** 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="afe71-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="afe71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afe71-107">EXAMPLES</span></span>

### <span data-ttu-id="afe71-108">Örnek 1: VMSS 'ye tanılama uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="afe71-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="afe71-109">Bu komut, VMSS 'ye bir tanılama uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="afe71-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="afe71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afe71-110">PARAMETERS</span></span>

### <span data-ttu-id="afe71-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="afe71-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="afe71-112">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="afe71-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="afe71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe71-113">-DefaultProfile</span></span>
<span data-ttu-id="afe71-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afe71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="afe71-115">-Force</span></span>
<span data-ttu-id="afe71-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="afe71-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afe71-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="afe71-117">-Name</span></span>
<span data-ttu-id="afe71-118">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afe71-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="afe71-119">-Protectedsettingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="afe71-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="afe71-120">Özel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="afe71-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="afe71-121">-Settingdosyayolu</span><span class="sxs-lookup"><span data-stu-id="afe71-121">-SettingFilePath</span></span>
<span data-ttu-id="afe71-122">Genel yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="afe71-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="afe71-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="afe71-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="afe71-124">Bu VMSS için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="afe71-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="afe71-125">Sürümü edinmek için, [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'Ini *PublisherName* parametresi ve *tür* parametresi için ıaasdiagnostics değeriyle çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="afe71-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="afe71-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afe71-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="afe71-127">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="afe71-127">Specify the VMSS object.</span></span>
<span data-ttu-id="afe71-128">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="afe71-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="afe71-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="afe71-129">-Confirm</span></span>
<span data-ttu-id="afe71-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afe71-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe71-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe71-131">-WhatIf</span></span>
<span data-ttu-id="afe71-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afe71-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe71-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afe71-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe71-134">CommonParameters</span></span>
<span data-ttu-id="afe71-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afe71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe71-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe71-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe71-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afe71-137">INPUTS</span></span>

### <span data-ttu-id="afe71-138">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afe71-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="afe71-139">System. String</span><span class="sxs-lookup"><span data-stu-id="afe71-139">System.String</span></span>

### <span data-ttu-id="afe71-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afe71-140">System.Boolean</span></span>

## <span data-ttu-id="afe71-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afe71-141">OUTPUTS</span></span>

### <span data-ttu-id="afe71-142">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afe71-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="afe71-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afe71-143">NOTES</span></span>

## <span data-ttu-id="afe71-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afe71-144">RELATED LINKS</span></span>

[<span data-ttu-id="afe71-145">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="afe71-145">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="afe71-146">Remove-azurermvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="afe71-146">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="afe71-147">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="afe71-147">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
