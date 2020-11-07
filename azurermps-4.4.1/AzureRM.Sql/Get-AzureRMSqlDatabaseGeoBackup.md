---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764764"
---
# <span data-ttu-id="205f6-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="205f6-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="205f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205f6-102">SYNOPSIS</span></span>
<span data-ttu-id="205f6-103">Bir veritabanının coğrafi yedekli yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="205f6-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="205f6-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="205f6-105">DESCRIPTION</span></span>
<span data-ttu-id="205f6-106">**Get-AzureRMSqlDatabaseGeoBackup** cmdlet 'i, belirtilen bir sunucuda bir SQL veritabanının belirtilen coğrafi ve yedekli yedek yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="205f6-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="205f6-107">Coğrafi olarak yedekli yedekleme, ayrı bir coğrafi konumdan veri dosyalarını kullanan geri yüklenebilen bir kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="205f6-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="205f6-108">Veritabanınızı yeni bir bölgeye kurtarmak için bölgesel kesinti olayında coğrafi artıklık yedeği geri yüklemek için Geo-Restore kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="205f6-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="205f6-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="205f6-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="205f6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="205f6-110">EXAMPLES</span></span>

### <span data-ttu-id="205f6-111">Örnek 1: sunucudaki tüm Coğrafi Yedekli yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="205f6-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="205f6-112">Bu komut, belirli bir sunucudaki tüm coğrafi artıklık yedekli yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="205f6-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="205f6-113">Örnek 2: belirtilen coğrafi</span><span class="sxs-lookup"><span data-stu-id="205f6-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="205f6-114">Bu komut, ContosoDatabase adlı veritabanı coğrafi artıklık yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="205f6-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="205f6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="205f6-115">PARAMETERS</span></span>

### <span data-ttu-id="205f6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="205f6-116">-DatabaseName</span></span>
<span data-ttu-id="205f6-117">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="205f6-117">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="205f6-119">SQL veritabanı sunucusunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="205f6-119">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="205f6-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="205f6-120">-ServerName</span></span>
<span data-ttu-id="205f6-121">Geri yüklenecek yedeklemeyi barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="205f6-121">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="205f6-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="205f6-122">-Confirm</span></span>
<span data-ttu-id="205f6-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="205f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205f6-124">-WhatIf</span></span>
<span data-ttu-id="205f6-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="205f6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205f6-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="205f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205f6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205f6-127">-DefaultProfile</span></span>
<span data-ttu-id="205f6-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="205f6-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="205f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205f6-129">CommonParameters</span></span>
<span data-ttu-id="205f6-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="205f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205f6-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205f6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205f6-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="205f6-132">INPUTS</span></span>

## <span data-ttu-id="205f6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="205f6-133">OUTPUTS</span></span>

### <span data-ttu-id="205f6-134">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackupmodel</span><span class="sxs-lookup"><span data-stu-id="205f6-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="205f6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="205f6-135">NOTES</span></span>

## <span data-ttu-id="205f6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="205f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="205f6-137">Genel Bakış: SQL veritabanıyla bulut iş devamlılık ve veritabanı olağanüstü durum kurtarması</span><span class="sxs-lookup"><span data-stu-id="205f6-137">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="205f6-138">Azure SQL veritabanını kesinti 'den kurtarma</span><span class="sxs-lookup"><span data-stu-id="205f6-138">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="205f6-139">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="205f6-139">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="205f6-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="205f6-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
