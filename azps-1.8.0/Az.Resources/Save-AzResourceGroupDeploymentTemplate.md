---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759319"
---
# <span data-ttu-id="bba89-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bba89-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="bba89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba89-102">SYNOPSIS</span></span>
<span data-ttu-id="bba89-103">Bir dosyaya kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bba89-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="bba89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bba89-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bba89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bba89-105">DESCRIPTION</span></span>
<span data-ttu-id="bba89-106">**Save-AzResourceGroupDeploymentTemplate** cmdlet 'ı bir JSON dosyasına kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bba89-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="bba89-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bba89-107">EXAMPLES</span></span>

### <span data-ttu-id="bba89-108">Örnek 1: Dağıtım şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="bba89-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="bba89-109">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bba89-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="bba89-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bba89-110">PARAMETERS</span></span>

### <span data-ttu-id="bba89-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bba89-111">-ApiVersion</span></span>
<span data-ttu-id="bba89-112">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bba89-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bba89-113">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bba89-113">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba89-114">-DefaultProfile</span></span>
<span data-ttu-id="bba89-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bba89-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bba89-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bba89-116">-DeploymentName</span></span>
<span data-ttu-id="bba89-117">Dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bba89-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bba89-118">-Force</span></span>
<span data-ttu-id="bba89-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bba89-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bba89-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="bba89-120">-Path</span></span>
<span data-ttu-id="bba89-121">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bba89-121">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-122">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bba89-122">-Pre</span></span>
<span data-ttu-id="bba89-123">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bba89-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="bba89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba89-124">-ResourceGroupName</span></span>
<span data-ttu-id="bba89-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bba89-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba89-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bba89-126">-Confirm</span></span>
<span data-ttu-id="bba89-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bba89-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba89-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba89-128">-WhatIf</span></span>
<span data-ttu-id="bba89-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bba89-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba89-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bba89-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba89-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba89-131">CommonParameters</span></span>
<span data-ttu-id="bba89-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bba89-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba89-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba89-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba89-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bba89-134">INPUTS</span></span>

### <span data-ttu-id="bba89-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bba89-135">System.String</span></span>

## <span data-ttu-id="bba89-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bba89-136">OUTPUTS</span></span>

### <span data-ttu-id="bba89-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bba89-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bba89-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bba89-138">NOTES</span></span>

## <span data-ttu-id="bba89-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bba89-139">RELATED LINKS</span></span>
