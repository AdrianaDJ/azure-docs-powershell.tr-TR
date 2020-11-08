---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268762"
---
# <span data-ttu-id="49fef-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="49fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49fef-102">SYNOPSIS</span></span>
<span data-ttu-id="49fef-103">Bir Azure SQL veritabanı yük devretme grubuna bir veya birden çok veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="49fef-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="49fef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49fef-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49fef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49fef-105">DESCRIPTION</span></span>
<span data-ttu-id="49fef-106">Azure SQL veritabanı yük devretme grubunun birincil sunucusundaki bir veya birden çok veritabanını o yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="49fef-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="49fef-107">Veritabanları var olan çoğaltma ilişkilerinde ikincil veritabanları olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="49fef-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="49fef-108">Komut, ekli veritabanlarının, yük devretme grubunun ikincil sunucusuna coğrafi olarak çoğaltılmasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="49fef-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="49fef-109">'-Database ' parametresini dolduracak veritabanı nesnelerini almak için, Get-AzSqlDatabase cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="49fef-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="49fef-110">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49fef-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="49fef-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49fef-111">EXAMPLES</span></span>

### <span data-ttu-id="49fef-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49fef-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="49fef-113">Bu komut bir veritabanını bir yük devretme grubuna atayarak ekler.</span><span class="sxs-lookup"><span data-stu-id="49fef-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="49fef-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49fef-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="49fef-115">Bu komut, sunucudaki tüm veritabanlarını bir yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="49fef-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="49fef-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="49fef-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="49fef-117">Bu komut, esnek havuzdaki tüm veritabanlarını bir yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="49fef-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="49fef-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49fef-118">PARAMETERS</span></span>

### <span data-ttu-id="49fef-119">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="49fef-119">-Database</span></span>
<span data-ttu-id="49fef-120">Yük devretme grubuna eklenecek bir veya birden çok Azure SQL veritabanı.</span><span class="sxs-lookup"><span data-stu-id="49fef-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49fef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fef-121">-DefaultProfile</span></span>
<span data-ttu-id="49fef-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="49fef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49fef-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="49fef-123">-FailoverGroupName</span></span>
<span data-ttu-id="49fef-124">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="49fef-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49fef-125">-ResourceGroupName</span></span>
<span data-ttu-id="49fef-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="49fef-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fef-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49fef-127">-ServerName</span></span>
<span data-ttu-id="49fef-128">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="49fef-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fef-129">CommonParameters</span></span>
<span data-ttu-id="49fef-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49fef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fef-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49fef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fef-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49fef-132">INPUTS</span></span>

### <span data-ttu-id="49fef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="49fef-133">System.String</span></span>

### <span data-ttu-id="49fef-134">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Sql. Database. model. Azurestabdatabasemodel, Microsoft. Azure. PowerShell. cmdlet. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="49fef-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="49fef-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49fef-135">OUTPUTS</span></span>

### <span data-ttu-id="49fef-136">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="49fef-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="49fef-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49fef-137">NOTES</span></span>

## <span data-ttu-id="49fef-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49fef-138">RELATED LINKS</span></span>

[<span data-ttu-id="49fef-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="49fef-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="49fef-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="49fef-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="49fef-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="49fef-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="49fef-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="49fef-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="49fef-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
