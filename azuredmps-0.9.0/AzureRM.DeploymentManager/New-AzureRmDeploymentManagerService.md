---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 25b4adeb2d62f1e66bd30cd990db27eadb41b405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572189"
---
# <span data-ttu-id="59572-101">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="59572-101">New-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="59572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59572-102">SYNOPSIS</span></span>
<span data-ttu-id="59572-103">Hizmet topolojisinde hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59572-103">Creates a service in a service topology.</span></span>

## <span data-ttu-id="59572-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59572-104">SYNTAX</span></span>

### <span data-ttu-id="59572-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59572-105">Interactive (Default)</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 -Name <String> -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59572-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="59572-106">ByServiceTopologyObject</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopology] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59572-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="59572-107">ByServiceTopologyResourceId</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59572-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59572-108">DESCRIPTION</span></span>
<span data-ttu-id="59572-109">**Yeni-AzureRmDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet oluşturur ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="59572-109">The **New-AzureRmDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="59572-110">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="59572-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="59572-111">Cmdlet bir hizmet nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="59572-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="59572-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59572-112">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="59572-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59572-113">EXAMPLES</span></span>

### <span data-ttu-id="59572-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59572-114">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="59572-115">Hizmet topolojisi altında ad ContosoService1 içeren yeni bir hizmet oluştururken, ABD 'deki konum Merkezi</span><span class="sxs-lookup"><span data-stu-id="59572-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="59572-116">TargetLocation özelliği, hizmet ContosoService1 'in belirtilen abonelikteki Doğu US bölgesine dağıtılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59572-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="59572-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59572-117">PARAMETERS</span></span>

### <span data-ttu-id="59572-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59572-118">-DefaultProfile</span></span>
<span data-ttu-id="59572-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59572-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59572-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="59572-120">-Location</span></span>
<span data-ttu-id="59572-121">Hizmet kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="59572-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59572-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="59572-122">-Name</span></span>
<span data-ttu-id="59572-123">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="59572-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59572-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59572-124">-ResourceGroupName</span></span>
<span data-ttu-id="59572-125">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="59572-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59572-126">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="59572-126">-ServiceTopology</span></span>
<span data-ttu-id="59572-127">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="59572-127">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="59572-128">-Servicetopologyıd</span><span class="sxs-lookup"><span data-stu-id="59572-128">-ServiceTopologyId</span></span>
<span data-ttu-id="59572-129">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="59572-129">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="59572-130">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="59572-130">-ServiceTopologyName</span></span>
<span data-ttu-id="59572-131">Bu hizmetin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="59572-131">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="59572-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="59572-132">-Tag</span></span>
<span data-ttu-id="59572-133">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="59572-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59572-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="59572-134">-TargetLocation</span></span>
<span data-ttu-id="59572-135">Hizmetin altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="59572-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59572-136">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="59572-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="59572-137">Hizmetin altındaki kaynakların dağıtılacağı aboneliği belirler.</span><span class="sxs-lookup"><span data-stu-id="59572-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59572-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="59572-138">-Confirm</span></span>
<span data-ttu-id="59572-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59572-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59572-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59572-140">-WhatIf</span></span>
<span data-ttu-id="59572-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59572-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59572-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59572-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59572-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59572-143">CommonParameters</span></span>
<span data-ttu-id="59572-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59572-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59572-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59572-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59572-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59572-146">INPUTS</span></span>

### <span data-ttu-id="59572-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59572-147">None</span></span>

## <span data-ttu-id="59572-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59572-148">OUTPUTS</span></span>

### <span data-ttu-id="59572-149">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="59572-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="59572-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59572-150">NOTES</span></span>

## <span data-ttu-id="59572-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59572-151">RELATED LINKS</span></span>

[<span data-ttu-id="59572-152">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="59572-152">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="59572-153">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="59572-153">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="59572-154">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="59572-154">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)