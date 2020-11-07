---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: 3db29e4ab0f2ab4afc9a3c29ef8ea0335ed5d528
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933896"
---
# <span data-ttu-id="c05b5-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c05b5-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="c05b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c05b5-103">Azure SQL yönetilen örnek veritabanı yedekli yedekleme hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="c05b5-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="c05b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c05b5-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c05b5-105">DESCRIPTION</span></span>
<span data-ttu-id="c05b5-106">**Get-Azsqlınstancedatabasegeobackup** cmdlet 'ı Azure SQL veritabanı yönetilen örneğinden bir veya birden çok Azure SQL veritabanı yedek yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="c05b5-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c05b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c05b5-107">EXAMPLES</span></span>

### <span data-ttu-id="c05b5-108">Örnek 1: bir örnekteki tüm veritabanı yedek yedeklerini alma</span><span class="sxs-lookup"><span data-stu-id="c05b5-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="c05b5-109">Bu komut, managedInstance1 adındaki örnekte tüm veritabanı yedek yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c05b5-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="c05b5-110">Örnek 2: yönetilen örnekte bir veritabanı yedek yedeği alma</span><span class="sxs-lookup"><span data-stu-id="c05b5-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="c05b5-111">Bu komut, managedInstance1 adındaki bir örnekten managedDatabase1 adındaki bir veritabanı yedek yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="c05b5-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="c05b5-112">Örnek 3: filtreleme kullanarak tüm veritabanı Artıklı yedekleri bir örneğe alma</span><span class="sxs-lookup"><span data-stu-id="c05b5-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="c05b5-113">Bu komut, managedInstance1 adındaki örnekte "managedDatabase" ile başlayan tüm veritabanı yedek yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c05b5-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="c05b5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c05b5-114">PARAMETERS</span></span>

### <span data-ttu-id="c05b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05b5-115">-DefaultProfile</span></span>
<span data-ttu-id="c05b5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c05b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05b5-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c05b5-117">-InstanceName</span></span>
<span data-ttu-id="c05b5-118">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="c05b5-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05b5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c05b5-119">-Name</span></span>
<span data-ttu-id="c05b5-120">Alınacak örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c05b5-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c05b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="c05b5-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c05b5-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05b5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05b5-123">CommonParameters</span></span>
<span data-ttu-id="c05b5-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c05b5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05b5-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c05b5-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05b5-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c05b5-126">INPUTS</span></span>

### <span data-ttu-id="c05b5-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c05b5-127">None</span></span>

## <span data-ttu-id="c05b5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c05b5-128">OUTPUTS</span></span>

### <span data-ttu-id="c05b5-129">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlrecoverablemanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="c05b5-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="c05b5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c05b5-130">NOTES</span></span>

## <span data-ttu-id="c05b5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c05b5-131">RELATED LINKS</span></span>
