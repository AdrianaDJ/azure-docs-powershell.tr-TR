---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275907"
---
# <span data-ttu-id="0b5ec-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0b5ec-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="0b5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5ec-103">Dağıtım işlemini alma</span><span class="sxs-lookup"><span data-stu-id="0b5ec-103">Get deployment operation</span></span>

## <span data-ttu-id="0b5ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b5ec-104">SYNTAX</span></span>

### <span data-ttu-id="0b5ec-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b5ec-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b5ec-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0b5ec-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b5ec-107">DESCRIPTION</span></span>
<span data-ttu-id="0b5ec-108">**Get-AzDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="0b5ec-109">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="0b5ec-110">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="0b5ec-111">İsteği ve yanıt içeriğini almak için, **Yeni-azdeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="0b5ec-112">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="0b5ec-113">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0b5ec-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="0b5ec-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b5ec-114">EXAMPLES</span></span>

### <span data-ttu-id="0b5ec-115">Örnek 1: dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="0b5ec-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="0b5ec-116">Geçerli abonelik kapsamındaki "test" adlı dağıtım işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="0b5ec-117">Örnek 2: dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="0b5ec-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="0b5ec-118">Bu komut, geçerli abonelik kapsamındaki "test" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="0b5ec-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b5ec-119">PARAMETERS</span></span>

### <span data-ttu-id="0b5ec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5ec-120">-DefaultProfile</span></span>
<span data-ttu-id="0b5ec-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b5ec-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0b5ec-122">-DeploymentName</span></span>
<span data-ttu-id="0b5ec-123">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-123">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5ec-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0b5ec-124">-DeploymentObject</span></span>
<span data-ttu-id="0b5ec-125">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-125">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5ec-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0b5ec-126">-OperationId</span></span>
<span data-ttu-id="0b5ec-127">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-127">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5ec-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0b5ec-128">-Pre</span></span>
<span data-ttu-id="0b5ec-129">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b5ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5ec-130">CommonParameters</span></span>
<span data-ttu-id="0b5ec-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5ec-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b5ec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5ec-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b5ec-133">INPUTS</span></span>

### <span data-ttu-id="0b5ec-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="0b5ec-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0b5ec-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b5ec-135">OUTPUTS</span></span>

### <span data-ttu-id="0b5ec-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0b5ec-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="0b5ec-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b5ec-137">NOTES</span></span>

## <span data-ttu-id="0b5ec-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b5ec-138">RELATED LINKS</span></span>
