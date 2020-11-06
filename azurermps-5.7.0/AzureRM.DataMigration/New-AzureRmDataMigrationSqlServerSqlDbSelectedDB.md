---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589808"
---
# <span data-ttu-id="32a2e-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="32a2e-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="32a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="32a2e-103">Geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir Migratesqlserversqldbdatabaseınput nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a2e-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32a2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32a2e-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="32a2e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="32a2e-106">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet 'i, geçiş için kaynak ve hedef veritabanları ve tablo eşlemelerinin yanı sıra tablo eşleştirmelerinin yanı sıra bir Migratesqlserversqldbdatabaseınput nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a2e-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="32a2e-107">Bu cmdlet, New-AzureRmDataMigrationTask cmdlet 'ini içeren bir parametre olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="32a2e-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="32a2e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32a2e-108">EXAMPLES</span></span>

### <span data-ttu-id="32a2e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="32a2e-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="32a2e-110">Yukarıdaki örnek, **AdventureWorks2016** veritabanını aynı ada sahıp bir SQL Azure veritabanına geçirmek Için Migratesqlserversqldbdatabaseınput nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a2e-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="32a2e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32a2e-111">PARAMETERS</span></span>

### <span data-ttu-id="32a2e-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="32a2e-112">-Confirm</span></span>
<span data-ttu-id="32a2e-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32a2e-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a2e-114">-DefaultProfile</span></span>
<span data-ttu-id="32a2e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32a2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a2e-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="32a2e-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="32a2e-117">Geçiş yapmadan önce veritabanını ReadOnly olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="32a2e-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a2e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="32a2e-118">-Name</span></span>
<span data-ttu-id="32a2e-119">Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="32a2e-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a2e-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="32a2e-120">-TableMap</span></span>
<span data-ttu-id="32a2e-121">kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="32a2e-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a2e-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="32a2e-122">-TargetDatabaseName</span></span>
<span data-ttu-id="32a2e-123">Hedef veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="32a2e-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="32a2e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32a2e-124">INPUTS</span></span>

### <span data-ttu-id="32a2e-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="32a2e-125">None</span></span>


## <span data-ttu-id="32a2e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32a2e-126">OUTPUTS</span></span>

### <span data-ttu-id="32a2e-127">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="32a2e-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="32a2e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32a2e-128">NOTES</span></span>

## <span data-ttu-id="32a2e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32a2e-129">RELATED LINKS</span></span>


