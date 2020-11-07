---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 07f6e9b01e3def2dfe7cc88602b9643344ff3c4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933675"
---
# <span data-ttu-id="db9b0-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="db9b0-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="db9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="db9b0-103">Bir veritabanının coğrafi yedekli yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="db9b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db9b0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db9b0-105">DESCRIPTION</span></span>
<span data-ttu-id="db9b0-106">**Get-AzSqlDatabaseGeoBackup** cmdlet 'i, belırlı bir SQL veritabanının veya belirtilen bir sunucuda bulunan tüm coğrafi artıklık yedekli yedeklemelerin belirtilen Coğrafi Yedekli yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="db9b0-107">Coğrafi olarak yedekli yedekleme, ayrı bir coğrafi konumdan veri dosyalarını kullanan geri yüklenebilen bir kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="db9b0-108">Veritabanınızı yeni bir bölgeye kurtarmak için bölgesel kesinti olayında coğrafi artıklık yedeği geri yüklemek için Geo-Restore kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db9b0-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="db9b0-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="db9b0-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="db9b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db9b0-110">EXAMPLES</span></span>

### <span data-ttu-id="db9b0-111">Örnek 1: sunucudaki tüm Coğrafi Yedekli yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="db9b0-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="db9b0-112">Bu komut, belirli bir sunucudaki tüm coğrafi artıklık yedekli yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="db9b0-113">Örnek 2: belirtilen coğrafi</span><span class="sxs-lookup"><span data-stu-id="db9b0-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="db9b0-114">Bu komut, ContosoDatabase adlı veritabanı coğrafi artıklık yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="db9b0-115">Örnek 3: filtreleme kullanarak sunucudaki tüm Coğrafi Yedekli yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="db9b0-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="db9b0-116">Bu komut, belirli bir sunucuda "contoso" ile başlayan tüm coğrafi artıklık yedekli yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="db9b0-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="db9b0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db9b0-117">PARAMETERS</span></span>

### <span data-ttu-id="db9b0-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db9b0-118">-DatabaseName</span></span>
<span data-ttu-id="db9b0-119">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9b0-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="db9b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9b0-120">-DefaultProfile</span></span>
<span data-ttu-id="db9b0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="db9b0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db9b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db9b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="db9b0-123">SQL veritabanı sunucusunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9b0-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="db9b0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db9b0-124">-ServerName</span></span>
<span data-ttu-id="db9b0-125">Geri yüklenecek yedeklemeyi barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9b0-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="db9b0-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="db9b0-126">-Confirm</span></span>
<span data-ttu-id="db9b0-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db9b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9b0-128">-WhatIf</span></span>
<span data-ttu-id="db9b0-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db9b0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db9b0-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db9b0-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9b0-131">CommonParameters</span></span>
<span data-ttu-id="db9b0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db9b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9b0-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db9b0-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9b0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db9b0-134">INPUTS</span></span>

### <span data-ttu-id="db9b0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="db9b0-135">System.String</span></span>

## <span data-ttu-id="db9b0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db9b0-136">OUTPUTS</span></span>

### <span data-ttu-id="db9b0-137">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackupmodel</span><span class="sxs-lookup"><span data-stu-id="db9b0-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="db9b0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db9b0-138">NOTES</span></span>

## <span data-ttu-id="db9b0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db9b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="db9b0-140">Genel Bakış: SQL veritabanıyla bulut iş devamlılık ve veritabanı olağanüstü durum kurtarması</span><span class="sxs-lookup"><span data-stu-id="db9b0-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="db9b0-141">Azure SQL veritabanını kesinti 'den kurtarma</span><span class="sxs-lookup"><span data-stu-id="db9b0-141">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="db9b0-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="db9b0-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="db9b0-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="db9b0-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
