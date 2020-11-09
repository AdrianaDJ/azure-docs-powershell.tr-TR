---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322834"
---
# <span data-ttu-id="fe2c0-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fe2c0-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="fe2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2c0-103">Dağıtım şablonunu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="fe2c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe2c0-104">SYNTAX</span></span>

### <span data-ttu-id="fe2c0-105">SaveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe2c0-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2c0-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fe2c0-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2c0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe2c0-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2c0-108">**Save-AzManagementGroupDeploymentTemplate** cmdlet 'i, bir dağıtım şablonunu bir yönetim grubundaki dağıtım IÇIN bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="fe2c0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe2c0-109">EXAMPLES</span></span>

### <span data-ttu-id="fe2c0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fe2c0-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="fe2c0-111">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="fe2c0-112">Örnek 2: dağıtım alma ve şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="fe2c0-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="fe2c0-113">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını alır ve şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="fe2c0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe2c0-114">PARAMETERS</span></span>

### <span data-ttu-id="fe2c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2c0-115">-DefaultProfile</span></span>
<span data-ttu-id="fe2c0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2c0-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="fe2c0-117">-DeploymentName</span></span>
<span data-ttu-id="fe2c0-118">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-118">The deployment name.</span></span>

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

### <span data-ttu-id="fe2c0-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fe2c0-119">-DeploymentObject</span></span>
<span data-ttu-id="fe2c0-120">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-120">The deployment object.</span></span>

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

### <span data-ttu-id="fe2c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe2c0-121">-Force</span></span>
<span data-ttu-id="fe2c0-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe2c0-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fe2c0-123">-ManagementGroupId</span></span>
<span data-ttu-id="fe2c0-124">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c0-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="fe2c0-125">-Path</span></span>
<span data-ttu-id="fe2c0-126">Şablon dosyasının çıkış yolu.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="fe2c0-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fe2c0-127">-Pre</span></span>
<span data-ttu-id="fe2c0-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fe2c0-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe2c0-129">-Confirm</span></span>
<span data-ttu-id="fe2c0-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2c0-131">-WhatIf</span></span>
<span data-ttu-id="fe2c0-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2c0-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2c0-134">CommonParameters</span></span>
<span data-ttu-id="fe2c0-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2c0-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2c0-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe2c0-137">INPUTS</span></span>

### <span data-ttu-id="fe2c0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="fe2c0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fe2c0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe2c0-139">OUTPUTS</span></span>

### <span data-ttu-id="fe2c0-140">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="fe2c0-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="fe2c0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe2c0-141">NOTES</span></span>

## <span data-ttu-id="fe2c0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe2c0-142">RELATED LINKS</span></span>
