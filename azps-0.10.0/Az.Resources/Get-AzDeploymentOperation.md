---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 1eafc934777809d7fd4041496b004ea682e97910
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936456"
---
# <span data-ttu-id="e0d72-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e0d72-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="e0d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d72-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d72-103">Dağıtım işlemini alma</span><span class="sxs-lookup"><span data-stu-id="e0d72-103">Get deployment operation</span></span>

## <span data-ttu-id="e0d72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0d72-104">SYNTAX</span></span>

### <span data-ttu-id="e0d72-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0d72-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0d72-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e0d72-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d72-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0d72-107">DESCRIPTION</span></span>
<span data-ttu-id="e0d72-108">**Get-AzDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="e0d72-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="e0d72-109">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="e0d72-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="e0d72-110">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="e0d72-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="e0d72-111">İsteği ve yanıt içeriğini almak için, **Yeni-azdeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e0d72-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="e0d72-112">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="e0d72-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="e0d72-113">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d72-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="e0d72-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0d72-114">EXAMPLES</span></span>

### <span data-ttu-id="e0d72-115">Dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="e0d72-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="e0d72-116">Geçerli abonelik kapsamındaki "test" adlı dağıtım işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="e0d72-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="e0d72-117">Dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="e0d72-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="e0d72-118">Bu komut, geçerli abonelik kapsamındaki "test" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0d72-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="e0d72-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0d72-119">PARAMETERS</span></span>

### <span data-ttu-id="e0d72-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e0d72-120">-ApiVersion</span></span>
<span data-ttu-id="e0d72-121">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0d72-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e0d72-122">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e0d72-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e0d72-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d72-123">-DefaultProfile</span></span>
<span data-ttu-id="e0d72-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0d72-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0d72-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e0d72-125">-DeploymentName</span></span>
<span data-ttu-id="e0d72-126">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="e0d72-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d72-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e0d72-127">-DeploymentObject</span></span>
<span data-ttu-id="e0d72-128">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e0d72-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d72-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e0d72-129">-OperationId</span></span>
<span data-ttu-id="e0d72-130">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="e0d72-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d72-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e0d72-131">-Pre</span></span>
<span data-ttu-id="e0d72-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0d72-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e0d72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d72-133">CommonParameters</span></span>
<span data-ttu-id="e0d72-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0d72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d72-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d72-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d72-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0d72-136">INPUTS</span></span>

### <span data-ttu-id="e0d72-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e0d72-137">System.String</span></span>
<span data-ttu-id="e0d72-138">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e0d72-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e0d72-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0d72-139">OUTPUTS</span></span>

### <span data-ttu-id="e0d72-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e0d72-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="e0d72-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0d72-141">NOTES</span></span>

## <span data-ttu-id="e0d72-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0d72-142">RELATED LINKS</span></span>