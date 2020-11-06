---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bcae25cba6eae5f883bffb7248cbca6f5516bcfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590605"
---
# <span data-ttu-id="e7418-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7418-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e7418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7418-102">SYNOPSIS</span></span>
<span data-ttu-id="e7418-103">Azure SQL veritabanı eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7418-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7418-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7418-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7418-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7418-105">DESCRIPTION</span></span>
<span data-ttu-id="e7418-106">**New-AzureRmSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7418-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e7418-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7418-107">EXAMPLES</span></span>

### <span data-ttu-id="e7418-108">Örnek 1: Azure SQL veritabanı için eşitleme grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7418-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="e7418-109">Bu komut, Azure SQL veritabanı için bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7418-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="e7418-110">"schema.json" yerel diskteki bir dosyadır.</span><span class="sxs-lookup"><span data-stu-id="e7418-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="e7418-111">JSON biçiminde Shema yükünü içerir.</span><span class="sxs-lookup"><span data-stu-id="e7418-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="e7418-112">JSON şemasının bir örneği: {"tablolar": [{"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}, "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="e7418-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="e7418-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7418-113">PARAMETERS</span></span>

### <span data-ttu-id="e7418-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7418-114">-Confirm</span></span>
<span data-ttu-id="e7418-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7418-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7418-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e7418-117">Eşitleme grubundaki hub ile üye veritabanı arasında çelişki çözme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="e7418-117">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7418-118">-DatabaseName</span></span>
<span data-ttu-id="e7418-119">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e7418-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e7418-120">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e7418-120">-DatabaseCredential</span></span>
<span data-ttu-id="e7418-121">Hub veritabanının SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e7418-121">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-122">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="e7418-122">-IntervalInSeconds</span></span>
<span data-ttu-id="e7418-123">Veri eşitlemesinin sıklığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="e7418-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="e7418-124">Varsayılan:-1; Yani otomatik eşitleme etkinleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e7418-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7418-125">-Name</span></span>
<span data-ttu-id="e7418-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e7418-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7418-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7418-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e7418-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7418-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="e7418-129">-SchemaFile</span></span>
<span data-ttu-id="e7418-130">Şema dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="e7418-130">The path of the schema file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7418-131">-ServerName</span></span>
<span data-ttu-id="e7418-132">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="e7418-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e7418-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7418-133">-SyncDatabaseName</span></span>
<span data-ttu-id="e7418-134">Eşitleme ile ilgili meta verileri depolamak için kullanılan veritabanı.</span><span class="sxs-lookup"><span data-stu-id="e7418-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7418-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="e7418-136">Eşitleme meta veri veritabanının ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e7418-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="e7418-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="e7418-138">Eşitleme meta veri veritabanının barındırıldığı sunucu.</span><span class="sxs-lookup"><span data-stu-id="e7418-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7418-139">-WhatIf</span></span>
<span data-ttu-id="e7418-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7418-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7418-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7418-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7418-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7418-142">-DefaultProfile</span></span>
<span data-ttu-id="e7418-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7418-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7418-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7418-144">CommonParameters</span></span>
<span data-ttu-id="e7418-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7418-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7418-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7418-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7418-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7418-147">INPUTS</span></span>

## <span data-ttu-id="e7418-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7418-148">OUTPUTS</span></span>

### <span data-ttu-id="e7418-149">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="e7418-149">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e7418-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7418-150">NOTES</span></span>

## <span data-ttu-id="e7418-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7418-151">RELATED LINKS</span></span>

[<span data-ttu-id="e7418-152">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7418-152">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e7418-153">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7418-153">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e7418-154">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7418-154">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

