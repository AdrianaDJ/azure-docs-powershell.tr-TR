---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096242"
---
# <span data-ttu-id="16edb-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="16edb-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="16edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16edb-102">SYNOPSIS</span></span>
<span data-ttu-id="16edb-103">Azure SQL veritabanı eşitleme grubunun günlüklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16edb-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="16edb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16edb-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16edb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16edb-105">DESCRIPTION</span></span>
<span data-ttu-id="16edb-106">**Get-AzSqlSyncGroupLog** cmdlet 'i, BIR Azure SQL veritabanı eşitleme grubunun günlüklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16edb-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="16edb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16edb-107">EXAMPLES</span></span>

### <span data-ttu-id="16edb-108">Örnek 1: Azure SQL eşitleme grubunun günlüklerini alma</span><span class="sxs-lookup"><span data-stu-id="16edb-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="16edb-109">Bu komut, bir Azure SQL eşitleme grubunun günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="16edb-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="16edb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16edb-110">PARAMETERS</span></span>

### <span data-ttu-id="16edb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16edb-111">-DatabaseName</span></span>
<span data-ttu-id="16edb-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="16edb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="16edb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16edb-113">-DefaultProfile</span></span>
<span data-ttu-id="16edb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16edb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16edb-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="16edb-115">-EndTime</span></span>
<span data-ttu-id="16edb-116">Günlüklerin Sorgulanacak bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="16edb-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16edb-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="16edb-117">-LogLevel</span></span>
<span data-ttu-id="16edb-118">Sorgulanacak günlüklerin türü.</span><span class="sxs-lookup"><span data-stu-id="16edb-118">The type of the logs to query.</span></span>
<span data-ttu-id="16edb-119">Geçerli değerler: ' hata ', ' uyarı ', ' başarı ' ve ' tümü '.</span><span class="sxs-lookup"><span data-stu-id="16edb-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16edb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16edb-120">-ResourceGroupName</span></span>
<span data-ttu-id="16edb-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="16edb-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="16edb-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16edb-122">-ServerName</span></span>
<span data-ttu-id="16edb-123">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="16edb-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="16edb-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="16edb-124">-StartTime</span></span>
<span data-ttu-id="16edb-125">Sorgunun sorgunun başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="16edb-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16edb-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="16edb-126">-SyncGroupName</span></span>
<span data-ttu-id="16edb-127">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16edb-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16edb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16edb-128">CommonParameters</span></span>
<span data-ttu-id="16edb-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16edb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16edb-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16edb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16edb-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16edb-131">INPUTS</span></span>

### <span data-ttu-id="16edb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="16edb-132">System.String</span></span>

## <span data-ttu-id="16edb-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16edb-133">OUTPUTS</span></span>

### <span data-ttu-id="16edb-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgrouplogmodel</span><span class="sxs-lookup"><span data-stu-id="16edb-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="16edb-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16edb-135">NOTES</span></span>

## <span data-ttu-id="16edb-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16edb-136">RELATED LINKS</span></span>
