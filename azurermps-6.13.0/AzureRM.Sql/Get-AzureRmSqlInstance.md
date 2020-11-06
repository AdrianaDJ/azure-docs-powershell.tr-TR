---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591880"
---
# <span data-ttu-id="98a41-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="98a41-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="98a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98a41-102">SYNOPSIS</span></span>
<span data-ttu-id="98a41-103">Azure SQL yönetilen veritabanı örneği hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="98a41-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98a41-104">SYNTAX</span></span>

### <span data-ttu-id="98a41-105">Getınstancebyresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98a41-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98a41-106">Getınstancebinaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="98a41-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="98a41-107">DESCRIPTION</span></span>
<span data-ttu-id="98a41-108">**Get-Azurermsqlınstance** cmdlet 'i, bir veya daha fazla Azure SQL yönetilen örneği hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="98a41-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="98a41-109">Yalnızca bu örneğin bilgilerini görmek için bir örneğin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="98a41-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="98a41-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98a41-110">EXAMPLES</span></span>

### <span data-ttu-id="98a41-111">Örnek 1: kaynak grubuna atanan tüm örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="98a41-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="98a41-112">Bu komut, ResourceGroup01 kaynak grubuna atanmış tüm örnekler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98a41-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="98a41-113">Örnek 2: örnek hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="98a41-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="98a41-114">Bu komut, managedInstance1 adlı örnek hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98a41-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="98a41-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98a41-115">PARAMETERS</span></span>

### <span data-ttu-id="98a41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a41-116">-DefaultProfile</span></span>
<span data-ttu-id="98a41-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98a41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a41-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="98a41-118">-Name</span></span>
<span data-ttu-id="98a41-119">SQL örneği adı.</span><span class="sxs-lookup"><span data-stu-id="98a41-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a41-120">-ResourceGroupName</span></span>
<span data-ttu-id="98a41-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="98a41-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a41-122">CommonParameters</span></span>
<span data-ttu-id="98a41-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98a41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a41-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a41-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a41-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98a41-125">INPUTS</span></span>

### <span data-ttu-id="98a41-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="98a41-126">None</span></span>

## <span data-ttu-id="98a41-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98a41-127">OUTPUTS</span></span>

### <span data-ttu-id="98a41-128">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="98a41-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="98a41-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98a41-129">NOTES</span></span>

## <span data-ttu-id="98a41-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98a41-130">RELATED LINKS</span></span>
