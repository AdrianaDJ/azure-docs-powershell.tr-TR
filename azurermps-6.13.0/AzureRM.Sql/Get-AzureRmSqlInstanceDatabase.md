---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590009"
---
# <span data-ttu-id="52d34-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="52d34-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="52d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d34-102">SYNOPSIS</span></span>
<span data-ttu-id="52d34-103">Azure SQL yönetilen örnek veritabanı hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="52d34-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d34-104">SYNTAX</span></span>

### <span data-ttu-id="52d34-105">Getınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52d34-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d34-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="52d34-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d34-107">Getınstancedatabasefromınstanceobject</span><span class="sxs-lookup"><span data-stu-id="52d34-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d34-108">DESCRIPTION</span></span>
<span data-ttu-id="52d34-109">**Get-Azurermsqlınstancedatabase** cmdlet 'i, BIR Azure SQL veritabanı yönetilen örneğindeki bir veya birden çok Azure SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="52d34-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="52d34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d34-110">EXAMPLES</span></span>

### <span data-ttu-id="52d34-111">Örnek 1: bir örnekteki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="52d34-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="52d34-112">Bu komut, managedInstance1 adındaki örnekte tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="52d34-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="52d34-113">Örnek 2: yönetilen örnekte bir veritabanını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="52d34-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="52d34-114">Bu komut, managedInstance1 adındaki bir örnekten managedDatabase1 adlı veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="52d34-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="52d34-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d34-115">PARAMETERS</span></span>

### <span data-ttu-id="52d34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d34-116">-DefaultProfile</span></span>
<span data-ttu-id="52d34-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52d34-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d34-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="52d34-118">-InstanceName</span></span>
<span data-ttu-id="52d34-119">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="52d34-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d34-120">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="52d34-120">-InstanceObject</span></span>
<span data-ttu-id="52d34-121">Örnek veritabanını almak için kullanılacak örnek nesne</span><span class="sxs-lookup"><span data-stu-id="52d34-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d34-122">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="52d34-122">-InstanceResourceId</span></span>
<span data-ttu-id="52d34-123">Alınacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="52d34-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d34-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="52d34-124">-Name</span></span>
<span data-ttu-id="52d34-125">Alınacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="52d34-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d34-126">-ResourceGroupName</span></span>
<span data-ttu-id="52d34-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="52d34-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d34-128">CommonParameters</span></span>
<span data-ttu-id="52d34-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d34-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d34-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d34-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d34-131">INPUTS</span></span>

### <span data-ttu-id="52d34-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52d34-132">System.String</span></span>
<span data-ttu-id="52d34-133">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="52d34-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="52d34-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d34-134">OUTPUTS</span></span>

### <span data-ttu-id="52d34-135">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="52d34-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="52d34-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d34-136">NOTES</span></span>

## <span data-ttu-id="52d34-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d34-137">RELATED LINKS</span></span>
