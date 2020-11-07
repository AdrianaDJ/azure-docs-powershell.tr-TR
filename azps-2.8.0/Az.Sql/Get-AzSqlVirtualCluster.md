---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933584"
---
# <span data-ttu-id="55047-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="55047-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="55047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55047-102">SYNOPSIS</span></span>
<span data-ttu-id="55047-103">Azure SQL sanal kümesi hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="55047-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="55047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55047-104">SYNTAX</span></span>

### <span data-ttu-id="55047-105">GetVirtualClusterByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55047-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55047-106">Getvirtualclusterbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="55047-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55047-107">Getvirtualclusterbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="55047-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55047-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55047-108">DESCRIPTION</span></span>
<span data-ttu-id="55047-109">**Get-AzSqlVirtualCluster** cmdlet 'i, bir veya daha fazla Azure SQL sanal kümesi hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="55047-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="55047-110">Yalnızca bu kümenin bilgilerini görmek için sanal kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="55047-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="55047-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55047-111">EXAMPLES</span></span>

### <span data-ttu-id="55047-112">Örnek 1: kaynak grubuna atanan tüm sanal kümeleri alma</span><span class="sxs-lookup"><span data-stu-id="55047-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="55047-113">Bu komut, kaynak grubu ResourceGroup01 atanan tüm Sanal kümeler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="55047-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="55047-114">Örnek 2: belirli sanal kümeyle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="55047-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="55047-115">Bu komut, kaynak grubundaki ResourceGroup01 sanal küme VirtualCluster1 hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="55047-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="55047-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55047-116">PARAMETERS</span></span>

### <span data-ttu-id="55047-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55047-117">-DefaultProfile</span></span>
<span data-ttu-id="55047-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55047-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55047-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="55047-119">-Name</span></span>
<span data-ttu-id="55047-120">Sanal kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="55047-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55047-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55047-121">-ResourceGroupName</span></span>
<span data-ttu-id="55047-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="55047-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55047-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55047-123">-ResourceId</span></span>
<span data-ttu-id="55047-124">Alınacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="55047-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55047-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55047-125">CommonParameters</span></span>
<span data-ttu-id="55047-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55047-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55047-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55047-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55047-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55047-128">INPUTS</span></span>

### <span data-ttu-id="55047-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55047-129">None</span></span>

## <span data-ttu-id="55047-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55047-130">OUTPUTS</span></span>

### <span data-ttu-id="55047-131">Microsoft. Azure. Commands. Sql. Virtu</span><span class="sxs-lookup"><span data-stu-id="55047-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="55047-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55047-132">NOTES</span></span>

## <span data-ttu-id="55047-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55047-133">RELATED LINKS</span></span>
