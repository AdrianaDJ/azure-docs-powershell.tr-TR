---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 2772f806ba5297ee9809a8800b25b4c42daf171e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592169"
---
# <span data-ttu-id="ad506-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="ad506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad506-102">SYNOPSIS</span></span>
<span data-ttu-id="ad506-103">Bir Azure SQL veritabanı yük devretme grubuna bir veya birden çok veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="ad506-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad506-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad506-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad506-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad506-105">DESCRIPTION</span></span>
<span data-ttu-id="ad506-106">Azure SQL veritabanı yük devretme grubunun birincil sunucusundaki bir veya birden çok veritabanını o yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="ad506-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="ad506-107">Veritabanları var olan çoğaltma ilişkilerinde ikincil veritabanları olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad506-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="ad506-108">Komut, ekli veritabanlarının, yük devretme grubunun ikincil sunucusuna coğrafi olarak çoğaltılmasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="ad506-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="ad506-109">'-Database ' parametresini dolduracak veritabanı nesnelerini almak için, Get-AzureRmSqlDatabase cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad506-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="ad506-110">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad506-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="ad506-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad506-111">EXAMPLES</span></span>

### <span data-ttu-id="ad506-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad506-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="ad506-113">Bu komut bir veritabanını bir yük devretme grubuna atayarak ekler.</span><span class="sxs-lookup"><span data-stu-id="ad506-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="ad506-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ad506-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="ad506-115">Bu komut, sunucudaki tüm veritabanlarını bir yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="ad506-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="ad506-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ad506-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="ad506-117">Bu komut, esnek havuzdaki tüm veritabanlarını bir yük devretme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="ad506-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="ad506-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad506-118">PARAMETERS</span></span>

### <span data-ttu-id="ad506-119">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="ad506-119">-Database</span></span>
<span data-ttu-id="ad506-120">Yük devretme grubuna eklenecek bir veya birden çok Azure SQL veritabanı.</span><span class="sxs-lookup"><span data-stu-id="ad506-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="ad506-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ad506-121">-FailoverGroupName</span></span>
<span data-ttu-id="ad506-122">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ad506-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ad506-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad506-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad506-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ad506-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad506-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ad506-125">-ServerName</span></span>
<span data-ttu-id="ad506-126">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="ad506-126">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ad506-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad506-127">-DefaultProfile</span></span>
<span data-ttu-id="ad506-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad506-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad506-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad506-129">CommonParameters</span></span>
<span data-ttu-id="ad506-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad506-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad506-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad506-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad506-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad506-132">INPUTS</span></span>

### <span data-ttu-id="ad506-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ad506-133">System.String</span></span>
<span data-ttu-id="ad506-134">System. Koleksiyonlar. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Sql. Database. model. Azuresıntab, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ad506-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ad506-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad506-135">OUTPUTS</span></span>

### <span data-ttu-id="ad506-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="ad506-136">System.Object</span></span>

## <span data-ttu-id="ad506-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad506-137">NOTES</span></span>

## <span data-ttu-id="ad506-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad506-138">RELATED LINKS</span></span>

[<span data-ttu-id="ad506-139">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ad506-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ad506-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ad506-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ad506-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ad506-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad506-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ad506-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ad506-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
