---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319758"
---
# <span data-ttu-id="6e2bc-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6e2bc-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="6e2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2bc-103">Azure SQL yönetilen örnek veritabanı hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6e2bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e2bc-104">SYNTAX</span></span>

### <span data-ttu-id="6e2bc-105">Getınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e2bc-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2bc-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2bc-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2bc-107">Getınstancedatabasefromınstanceobject</span><span class="sxs-lookup"><span data-stu-id="6e2bc-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e2bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e2bc-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2bc-109">**Get-Azsqlınstancedatabase** cmdlet 'ı BIR Azure SQL veritabanı yönetilen örneğinden bir veya birden çok Azure SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="6e2bc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e2bc-110">EXAMPLES</span></span>

### <span data-ttu-id="6e2bc-111">Örnek 1: bir örnekteki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="6e2bc-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="6e2bc-112">Bu komut, managedInstance1 adındaki örnekte tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="6e2bc-113">Örnek 2: yönetilen örnekte bir veritabanını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="6e2bc-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="6e2bc-114">Bu komut, managedInstance1 adındaki bir örnekten managedDatabase1 adlı veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="6e2bc-115">Örnek 3: filtreleme kullanarak bir örnekteki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="6e2bc-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="6e2bc-116">Bu komut, managedInstance1 adındaki örnekte "managedDatabase" ile başlayan tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="6e2bc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e2bc-117">PARAMETERS</span></span>

### <span data-ttu-id="6e2bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2bc-118">-DefaultProfile</span></span>
<span data-ttu-id="6e2bc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2bc-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6e2bc-120">-InstanceName</span></span>
<span data-ttu-id="6e2bc-121">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2bc-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="6e2bc-122">-InstanceObject</span></span>
<span data-ttu-id="6e2bc-123">Örnek veritabanını almak için kullanılacak örnek nesne</span><span class="sxs-lookup"><span data-stu-id="6e2bc-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2bc-124">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="6e2bc-124">-InstanceResourceId</span></span>
<span data-ttu-id="6e2bc-125">Alınacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6e2bc-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2bc-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e2bc-126">-Name</span></span>
<span data-ttu-id="6e2bc-127">Alınacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e2bc-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2bc-130">CommonParameters</span></span>
<span data-ttu-id="6e2bc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2bc-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2bc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e2bc-133">INPUTS</span></span>

### <span data-ttu-id="6e2bc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6e2bc-134">System.String</span></span>

### <span data-ttu-id="6e2bc-135">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="6e2bc-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="6e2bc-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e2bc-136">OUTPUTS</span></span>

### <span data-ttu-id="6e2bc-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="6e2bc-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6e2bc-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e2bc-138">NOTES</span></span>

## <span data-ttu-id="6e2bc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e2bc-139">RELATED LINKS</span></span>
