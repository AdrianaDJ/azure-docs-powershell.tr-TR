---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 79f71c31f1a04b350733465338e9edcbd281af5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752622"
---
# <span data-ttu-id="2ed2e-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2ed2e-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="2ed2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed2e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed2e-103">Kapsayıcı grupları alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-103">Gets container groups.</span></span>

## <span data-ttu-id="2ed2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ed2e-104">SYNTAX</span></span>

### <span data-ttu-id="2ed2e-105">ListContainerGroupParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ed2e-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ed2e-106">Getcontainergroupınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="2ed2e-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ed2e-107">Getcontainergroupbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="2ed2e-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ed2e-108">DESCRIPTION</span></span>
<span data-ttu-id="2ed2e-109">**Get-AzContainerGroup** cmdlet 'i, bir kaynak grubundaki veya abonelikteki belirli bir kapsayıcı grubunu veya tüm kapsayıcı grupları alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="2ed2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ed2e-110">EXAMPLES</span></span>

### <span data-ttu-id="2ed2e-111">Örnek 1: belirtilen kapsayıcı grubunu alır</span><span class="sxs-lookup"><span data-stu-id="2ed2e-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="2ed2e-112">Komut belirtilen kapsayıcı grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="2ed2e-113">Örnek 2: kaynak grubundaki kapsayıcı gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="2ed2e-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="2ed2e-114">Bu komut, kaynak grubundaki kapsayıcı gruplarını alır `demo` .</span><span class="sxs-lookup"><span data-stu-id="2ed2e-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="2ed2e-115">Örnek 3: geçerli abonelikteki kapsayıcı gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="2ed2e-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="2ed2e-116">Bu komut, geçerli abonelikteki kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="2ed2e-117">Örnek 4: kaynak kimliğini kullanarak kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="2ed2e-118">Bu komut, kapsayıcı grubu kaynak kimliğiyle alır.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="2ed2e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ed2e-119">PARAMETERS</span></span>

### <span data-ttu-id="2ed2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed2e-120">-DefaultProfile</span></span>
<span data-ttu-id="2ed2e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed2e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ed2e-122">-Name</span></span>
<span data-ttu-id="2ed2e-123">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ed2e-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed2e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ed2e-126">-ResourceId</span></span>
<span data-ttu-id="2ed2e-127">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed2e-128">CommonParameters</span></span>
<span data-ttu-id="2ed2e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ed2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed2e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed2e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed2e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ed2e-131">INPUTS</span></span>

### <span data-ttu-id="2ed2e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ed2e-132">System.String</span></span>

## <span data-ttu-id="2ed2e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ed2e-133">OUTPUTS</span></span>

### <span data-ttu-id="2ed2e-134">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2ed2e-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2ed2e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ed2e-135">NOTES</span></span>

## <span data-ttu-id="2ed2e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ed2e-136">RELATED LINKS</span></span>
