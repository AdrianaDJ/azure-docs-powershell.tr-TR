---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: 665fcc30b0b9c2769af66ae4a590f3526438cae6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586755"
---
# <span data-ttu-id="cf4c8-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="cf4c8-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="cf4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4c8-103">Kapsayıcı grupları alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf4c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf4c8-104">SYNTAX</span></span>

### <span data-ttu-id="cf4c8-105">ListContainerGroupParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf4c8-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf4c8-106">Getcontainergroupınresourcegroupparamset</span><span class="sxs-lookup"><span data-stu-id="cf4c8-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf4c8-107">Getcontainergroupbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="cf4c8-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf4c8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf4c8-108">DESCRIPTION</span></span>
<span data-ttu-id="cf4c8-109">**Get-AzureRmContainerGroup** cmdlet 'i, bir kaynak grubundaki veya abonelikteki belirli bir kapsayıcı grubunu veya tüm kapsayıcı grupları alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="cf4c8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf4c8-110">EXAMPLES</span></span>

### <span data-ttu-id="cf4c8-111">Örnek 1: belirtilen kapsayıcı grubunu alır</span><span class="sxs-lookup"><span data-stu-id="cf4c8-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

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

<span data-ttu-id="cf4c8-112">Komut belirtilen kapsayıcı grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="cf4c8-113">Örnek 2: kaynak grubundaki kapsayıcı gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="cf4c8-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="cf4c8-114">Bu komut, kaynak grubundaki kapsayıcı gruplarını alır `demo` .</span><span class="sxs-lookup"><span data-stu-id="cf4c8-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="cf4c8-115">Örnek 3: geçerli abonelikteki kapsayıcı gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="cf4c8-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="cf4c8-116">Bu komut, geçerli abonelikteki kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="cf4c8-117">Örnek 4: kaynak kimliğini kullanarak kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

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

<span data-ttu-id="cf4c8-118">Bu komut, kapsayıcı grubu kaynak kimliğiyle alır.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="cf4c8-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf4c8-119">PARAMETERS</span></span>

### <span data-ttu-id="cf4c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4c8-120">-DefaultProfile</span></span>
<span data-ttu-id="cf4c8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf4c8-122">-Name</span></span>
<span data-ttu-id="cf4c8-123">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-123">The container group Name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf4c8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-125">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf4c8-126">-ResourceId</span></span>
<span data-ttu-id="cf4c8-127">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4c8-128">CommonParameters</span></span>
<span data-ttu-id="cf4c8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4c8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf4c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4c8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf4c8-131">INPUTS</span></span>

### <span data-ttu-id="cf4c8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cf4c8-132">System.String</span></span>

## <span data-ttu-id="cf4c8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf4c8-133">OUTPUTS</span></span>

### <span data-ttu-id="cf4c8-134">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="cf4c8-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="cf4c8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf4c8-135">NOTES</span></span>

## <span data-ttu-id="cf4c8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf4c8-136">RELATED LINKS</span></span>
