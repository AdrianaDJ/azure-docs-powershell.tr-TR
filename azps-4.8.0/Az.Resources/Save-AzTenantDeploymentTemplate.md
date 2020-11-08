---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: 79a60294126a990d191e4838a91c0f6554bea43b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266405"
---
# <span data-ttu-id="205e7-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="205e7-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="205e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205e7-102">SYNOPSIS</span></span>
<span data-ttu-id="205e7-103">Dağıtım şablonunu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="205e7-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="205e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="205e7-104">SYNTAX</span></span>

### <span data-ttu-id="205e7-105">SaveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="205e7-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205e7-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="205e7-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="205e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="205e7-107">DESCRIPTION</span></span>
<span data-ttu-id="205e7-108">**Save-AzTenantDeploymentTemplate** cmdlet 'i, kiracı kapsamındaki bir dağıtım için bir DAĞıTıM şablonunu JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="205e7-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="205e7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="205e7-109">EXAMPLES</span></span>

### <span data-ttu-id="205e7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="205e7-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="205e7-111">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="205e7-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="205e7-112">Örnek 2: dağıtım alma ve şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="205e7-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="205e7-113">Bu komut, geçerli kiracı kapsamındaki "RolesDeployment" dağıtımını alır ve şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="205e7-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="205e7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="205e7-114">PARAMETERS</span></span>

### <span data-ttu-id="205e7-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="205e7-115">-ApiVersion</span></span>
<span data-ttu-id="205e7-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="205e7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="205e7-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="205e7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="205e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205e7-118">-DefaultProfile</span></span>
<span data-ttu-id="205e7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="205e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205e7-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="205e7-120">-DeploymentName</span></span>
<span data-ttu-id="205e7-121">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="205e7-121">The deployment name.</span></span>

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

### <span data-ttu-id="205e7-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="205e7-122">-DeploymentObject</span></span>
<span data-ttu-id="205e7-123">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="205e7-123">The deployment object.</span></span>

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

### <span data-ttu-id="205e7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="205e7-124">-Force</span></span>
<span data-ttu-id="205e7-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="205e7-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="205e7-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="205e7-126">-Path</span></span>
<span data-ttu-id="205e7-127">Şablon dosyasının çıkış yolu.</span><span class="sxs-lookup"><span data-stu-id="205e7-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="205e7-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="205e7-128">-Pre</span></span>
<span data-ttu-id="205e7-129">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="205e7-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="205e7-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="205e7-130">-Confirm</span></span>
<span data-ttu-id="205e7-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="205e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205e7-132">-WhatIf</span></span>
<span data-ttu-id="205e7-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="205e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205e7-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="205e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205e7-135">CommonParameters</span></span>
<span data-ttu-id="205e7-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="205e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205e7-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="205e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205e7-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="205e7-138">INPUTS</span></span>

### <span data-ttu-id="205e7-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="205e7-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="205e7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="205e7-140">OUTPUTS</span></span>

### <span data-ttu-id="205e7-141">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="205e7-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="205e7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="205e7-142">NOTES</span></span>

## <span data-ttu-id="205e7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="205e7-143">RELATED LINKS</span></span>
