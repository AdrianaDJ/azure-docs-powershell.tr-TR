---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279815"
---
# <span data-ttu-id="5324f-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="5324f-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="5324f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5324f-102">SYNOPSIS</span></span>
<span data-ttu-id="5324f-103">Dağıtım şablonunu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5324f-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="5324f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5324f-104">SYNTAX</span></span>

### <span data-ttu-id="5324f-105">SaveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5324f-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5324f-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5324f-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5324f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5324f-107">DESCRIPTION</span></span>
<span data-ttu-id="5324f-108">**Save-AzDeploymentTemplate** cmdlet 'i bir dağıtım ŞABLONUNU bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5324f-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="5324f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5324f-109">EXAMPLES</span></span>

### <span data-ttu-id="5324f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5324f-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="5324f-111">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5324f-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="5324f-112">Örnek 2: dağıtım alma ve şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="5324f-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="5324f-113">Bu komut, geçerli abonelik kapsamındaki "RolesDeployment" dağıtımını alır ve şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5324f-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="5324f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5324f-114">PARAMETERS</span></span>

### <span data-ttu-id="5324f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5324f-115">-DefaultProfile</span></span>
<span data-ttu-id="5324f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5324f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5324f-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5324f-117">-DeploymentName</span></span>
<span data-ttu-id="5324f-118">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="5324f-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5324f-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5324f-119">-DeploymentObject</span></span>
<span data-ttu-id="5324f-120">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5324f-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5324f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5324f-121">-Force</span></span>
<span data-ttu-id="5324f-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5324f-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5324f-123">-Yol</span><span class="sxs-lookup"><span data-stu-id="5324f-123">-Path</span></span>
<span data-ttu-id="5324f-124">Şablon dosyasının çıkış yolu.</span><span class="sxs-lookup"><span data-stu-id="5324f-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="5324f-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="5324f-125">-Pre</span></span>
<span data-ttu-id="5324f-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5324f-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5324f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="5324f-127">-Confirm</span></span>
<span data-ttu-id="5324f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5324f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5324f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5324f-129">-WhatIf</span></span>
<span data-ttu-id="5324f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5324f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5324f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5324f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5324f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5324f-132">CommonParameters</span></span>
<span data-ttu-id="5324f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5324f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5324f-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5324f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5324f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5324f-135">INPUTS</span></span>

### <span data-ttu-id="5324f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="5324f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5324f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5324f-137">OUTPUTS</span></span>

### <span data-ttu-id="5324f-138">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="5324f-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="5324f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5324f-139">NOTES</span></span>

## <span data-ttu-id="5324f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5324f-140">RELATED LINKS</span></span>
