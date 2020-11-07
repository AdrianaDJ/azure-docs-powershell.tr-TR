---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752150"
---
# <span data-ttu-id="58498-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="58498-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="58498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58498-102">SYNOPSIS</span></span>
<span data-ttu-id="58498-103">Hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="58498-103">Gets the service.</span></span>

## <span data-ttu-id="58498-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58498-104">SYNTAX</span></span>

### <span data-ttu-id="58498-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58498-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58498-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="58498-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58498-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="58498-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58498-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="58498-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58498-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="58498-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58498-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="58498-110">DESCRIPTION</span></span>
<span data-ttu-id="58498-111">**Get-AzDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet alır ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="58498-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="58498-112">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="58498-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="58498-113">Alternatif olarak, servis nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58498-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="58498-114">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58498-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="58498-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58498-115">EXAMPLES</span></span>

### <span data-ttu-id="58498-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58498-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="58498-117">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde alır.</span><span class="sxs-lookup"><span data-stu-id="58498-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="58498-118">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet alma.</span><span class="sxs-lookup"><span data-stu-id="58498-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="58498-119">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde alır.</span><span class="sxs-lookup"><span data-stu-id="58498-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="58498-120">Örnek 3: hizmet nesnesini kullanarak hizmet alma.</span><span class="sxs-lookup"><span data-stu-id="58498-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="58498-121">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="58498-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="58498-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58498-122">PARAMETERS</span></span>

### <span data-ttu-id="58498-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58498-123">-DefaultProfile</span></span>
<span data-ttu-id="58498-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58498-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58498-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58498-125">-InputObject</span></span>
<span data-ttu-id="58498-126">Hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="58498-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58498-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="58498-127">-Name</span></span>
<span data-ttu-id="58498-128">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="58498-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58498-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58498-129">-ResourceGroupName</span></span>
<span data-ttu-id="58498-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="58498-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58498-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="58498-131">-ResourceId</span></span>
<span data-ttu-id="58498-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="58498-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58498-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="58498-133">-ServiceTopologyName</span></span>
<span data-ttu-id="58498-134">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="58498-134">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58498-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="58498-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="58498-136">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="58498-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58498-137">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="58498-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="58498-138">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="58498-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58498-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58498-139">CommonParameters</span></span>
<span data-ttu-id="58498-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58498-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58498-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58498-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58498-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58498-142">INPUTS</span></span>

### <span data-ttu-id="58498-143">System. String</span><span class="sxs-lookup"><span data-stu-id="58498-143">System.String</span></span>

### <span data-ttu-id="58498-144">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="58498-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="58498-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58498-145">OUTPUTS</span></span>

### <span data-ttu-id="58498-146">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="58498-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="58498-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58498-147">NOTES</span></span>

## <span data-ttu-id="58498-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58498-148">RELATED LINKS</span></span>
