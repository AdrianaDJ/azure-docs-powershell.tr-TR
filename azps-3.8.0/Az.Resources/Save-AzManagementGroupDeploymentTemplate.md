---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: 536d8f0d7f92e4ca880998293d74d0fc2f1617f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097225"
---
# <span data-ttu-id="846a4-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="846a4-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="846a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="846a4-102">SYNOPSIS</span></span>
<span data-ttu-id="846a4-103">Dağıtım şablonunu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="846a4-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="846a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="846a4-104">SYNTAX</span></span>

### <span data-ttu-id="846a4-105">SaveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="846a4-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="846a4-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="846a4-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="846a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="846a4-107">DESCRIPTION</span></span>
<span data-ttu-id="846a4-108">**Save-AzManagementGroupDeploymentTemplate** cmdlet 'i, bir dağıtım şablonunu bir yönetim grubundaki dağıtım IÇIN bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="846a4-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="846a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="846a4-109">EXAMPLES</span></span>

### <span data-ttu-id="846a4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="846a4-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="846a4-111">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="846a4-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="846a4-112">Örnek 2: dağıtım alma ve şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="846a4-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="846a4-113">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını alır ve şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="846a4-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="846a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="846a4-114">PARAMETERS</span></span>

### <span data-ttu-id="846a4-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="846a4-115">-ApiVersion</span></span>
<span data-ttu-id="846a4-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="846a4-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="846a4-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="846a4-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="846a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846a4-118">-DefaultProfile</span></span>
<span data-ttu-id="846a4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="846a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="846a4-120">-DeploymentName</span></span>
<span data-ttu-id="846a4-121">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="846a4-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="846a4-122">-DeploymentObject</span></span>
<span data-ttu-id="846a4-123">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="846a4-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="846a4-124">-Force</span></span>
<span data-ttu-id="846a4-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="846a4-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="846a4-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="846a4-126">-ManagementGroupId</span></span>
<span data-ttu-id="846a4-127">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="846a4-127">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="846a4-128">-Path</span></span>
<span data-ttu-id="846a4-129">Şablon dosyasının çıkış yolu.</span><span class="sxs-lookup"><span data-stu-id="846a4-129">The output path of the template file.</span></span>

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

### <span data-ttu-id="846a4-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="846a4-130">-Pre</span></span>
<span data-ttu-id="846a4-131">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="846a4-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="846a4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="846a4-132">-Confirm</span></span>
<span data-ttu-id="846a4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="846a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846a4-134">-WhatIf</span></span>
<span data-ttu-id="846a4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="846a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="846a4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="846a4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846a4-137">CommonParameters</span></span>
<span data-ttu-id="846a4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="846a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846a4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="846a4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846a4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="846a4-140">INPUTS</span></span>

### <span data-ttu-id="846a4-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="846a4-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="846a4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="846a4-142">OUTPUTS</span></span>

### <span data-ttu-id="846a4-143">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="846a4-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="846a4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="846a4-144">NOTES</span></span>

## <span data-ttu-id="846a4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="846a4-145">RELATED LINKS</span></span>
