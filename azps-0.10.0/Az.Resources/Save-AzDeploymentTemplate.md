---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 82fd6ba15a240be208445493810551154e188e92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936327"
---
# <span data-ttu-id="d1b3a-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d1b3a-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="d1b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b3a-103">Dağıtım şablonunu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="d1b3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1b3a-104">SYNTAX</span></span>

### <span data-ttu-id="d1b3a-105">SaveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1b3a-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1b3a-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d1b3a-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="d1b3a-108">**Save-AzDeploymentTemplate** cmdlet 'i bir dağıtım ŞABLONUNU bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="d1b3a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1b3a-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b3a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1b3a-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="d1b3a-111">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="d1b3a-112">Örnek 2: dağıtım alma ve şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="d1b3a-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="d1b3a-113">Bu komut, geçerli abonelik kapsamındaki "RolesDeployment" dağıtımını alır ve şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="d1b3a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1b3a-114">PARAMETERS</span></span>

### <span data-ttu-id="d1b3a-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="d1b3a-115">-ApiVersion</span></span>
<span data-ttu-id="d1b3a-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d1b3a-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d1b3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b3a-118">-DefaultProfile</span></span>
<span data-ttu-id="d1b3a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b3a-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d1b3a-120">-DeploymentName</span></span>
<span data-ttu-id="d1b3a-121">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-121">The deployment name.</span></span>

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

### <span data-ttu-id="d1b3a-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d1b3a-122">-DeploymentObject</span></span>
<span data-ttu-id="d1b3a-123">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-123">The deployment object.</span></span>

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

### <span data-ttu-id="d1b3a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d1b3a-124">-Force</span></span>
<span data-ttu-id="d1b3a-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d1b3a-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="d1b3a-126">-Path</span></span>
<span data-ttu-id="d1b3a-127">Şablon dosyasının çıkış yolu.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="d1b3a-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="d1b3a-128">-Pre</span></span>
<span data-ttu-id="d1b3a-129">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d1b3a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1b3a-130">-Confirm</span></span>
<span data-ttu-id="d1b3a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b3a-132">-WhatIf</span></span>
<span data-ttu-id="d1b3a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1b3a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b3a-135">CommonParameters</span></span>
<span data-ttu-id="d1b3a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1b3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b3a-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b3a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b3a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1b3a-138">INPUTS</span></span>

### <span data-ttu-id="d1b3a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1b3a-139">System.String</span></span>

## <span data-ttu-id="d1b3a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1b3a-140">OUTPUTS</span></span>

### <span data-ttu-id="d1b3a-141">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodelleri</span><span class="sxs-lookup"><span data-stu-id="d1b3a-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="d1b3a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1b3a-142">NOTES</span></span>

## <span data-ttu-id="d1b3a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1b3a-143">RELATED LINKS</span></span>
