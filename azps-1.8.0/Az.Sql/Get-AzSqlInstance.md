---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758979"
---
# <span data-ttu-id="66861-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="66861-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="66861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66861-102">SYNOPSIS</span></span>
<span data-ttu-id="66861-103">Azure SQL yönetilen veritabanı örneği hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="66861-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="66861-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66861-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66861-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66861-105">DESCRIPTION</span></span>
<span data-ttu-id="66861-106">**Get-Azsqlınstance** cmdlet 'i, bir veya daha fazla Azure SQL yönetilen örneği hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="66861-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="66861-107">Yalnızca bu örneğin bilgilerini görmek için bir örneğin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="66861-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="66861-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66861-108">EXAMPLES</span></span>

### <span data-ttu-id="66861-109">Örnek 1: kaynak grubuna atanan tüm örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="66861-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="66861-110">Bu komut, ResourceGroup01 kaynak grubuna atanmış tüm örnekler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="66861-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="66861-111">Örnek 2: örnek hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="66861-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="66861-112">Bu komut, managedInstance1 adlı örnek hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="66861-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="66861-113">Örnek 3: filtreleme kullanarak kaynak grubuna atanan tüm örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="66861-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="66861-114">Bu komut, "ManagedInstance" ile başlayan kaynak grubu ResourceGroup01 atanan tüm örnekler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="66861-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="66861-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66861-115">PARAMETERS</span></span>

### <span data-ttu-id="66861-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66861-116">-DefaultProfile</span></span>
<span data-ttu-id="66861-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66861-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66861-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="66861-118">-Name</span></span>
<span data-ttu-id="66861-119">SQL örneği adı.</span><span class="sxs-lookup"><span data-stu-id="66861-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="66861-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66861-120">-ResourceGroupName</span></span>
<span data-ttu-id="66861-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66861-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="66861-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66861-122">CommonParameters</span></span>
<span data-ttu-id="66861-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66861-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66861-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66861-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66861-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66861-125">INPUTS</span></span>

### <span data-ttu-id="66861-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="66861-126">None</span></span>

## <span data-ttu-id="66861-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66861-127">OUTPUTS</span></span>

### <span data-ttu-id="66861-128">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="66861-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="66861-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66861-129">NOTES</span></span>

## <span data-ttu-id="66861-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66861-130">RELATED LINKS</span></span>
