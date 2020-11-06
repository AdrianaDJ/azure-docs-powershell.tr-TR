---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: f8a939dbaac0dadb52aff28b208f7fb69ef836df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592388"
---
# <span data-ttu-id="1c96e-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="1c96e-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="1c96e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c96e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c96e-103">Azure SQL veritabanı eşitleme grubunun günlüklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c96e-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c96e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c96e-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c96e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c96e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c96e-106">**Get-AzureRmSqlSyncGroupLog** cmdlet 'i, BIR Azure SQL veritabanı eşitleme grubunun günlüklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c96e-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1c96e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c96e-107">EXAMPLES</span></span>

### <span data-ttu-id="1c96e-108">Örnek 1: Azure SQL eşitleme grubunun günlüklerini alma</span><span class="sxs-lookup"><span data-stu-id="1c96e-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="1c96e-109">Bu komut, bir Azure SQL eşitleme grubunun günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="1c96e-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="1c96e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c96e-110">PARAMETERS</span></span>

### <span data-ttu-id="1c96e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c96e-111">-DatabaseName</span></span>
<span data-ttu-id="1c96e-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1c96e-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c96e-113">-DefaultProfile</span></span>
<span data-ttu-id="1c96e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1c96e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c96e-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="1c96e-115">-EndTime</span></span>
<span data-ttu-id="1c96e-116">Günlüklerin Sorgulanacak bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="1c96e-116">The end time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="1c96e-117">-LogLevel</span></span>
<span data-ttu-id="1c96e-118">Sorgulanacak günlüklerin türü.</span><span class="sxs-lookup"><span data-stu-id="1c96e-118">The type of the logs to query.</span></span>
<span data-ttu-id="1c96e-119">Geçerli değerler: ' hata ', ' uyarı ', ' başarı ' ve ' tümü '.</span><span class="sxs-lookup"><span data-stu-id="1c96e-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c96e-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c96e-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1c96e-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c96e-122">-ServerName</span></span>
<span data-ttu-id="1c96e-123">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="1c96e-123">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1c96e-124">-StartTime</span></span>
<span data-ttu-id="1c96e-125">Sorgunun sorgunun başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="1c96e-125">The start time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1c96e-126">-SyncGroupName</span></span>
<span data-ttu-id="1c96e-127">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1c96e-127">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c96e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c96e-128">CommonParameters</span></span>
<span data-ttu-id="1c96e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c96e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c96e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c96e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c96e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c96e-131">INPUTS</span></span>

### <span data-ttu-id="1c96e-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1c96e-132">None</span></span>
<span data-ttu-id="1c96e-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1c96e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c96e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c96e-134">OUTPUTS</span></span>

### <span data-ttu-id="1c96e-135">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgrouplogmodel</span><span class="sxs-lookup"><span data-stu-id="1c96e-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="1c96e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c96e-136">NOTES</span></span>

## <span data-ttu-id="1c96e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c96e-137">RELATED LINKS</span></span>
