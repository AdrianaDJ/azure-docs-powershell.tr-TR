---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 512ed43ac1770a7a1a026c5a64d20a25016d547e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758871"
---
# <span data-ttu-id="1db23-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1db23-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="1db23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db23-102">SYNOPSIS</span></span>
<span data-ttu-id="1db23-103">Azure SQL veritabanı eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1db23-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1db23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1db23-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1db23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db23-105">DESCRIPTION</span></span>
<span data-ttu-id="1db23-106">**New-AzSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1db23-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1db23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1db23-107">EXAMPLES</span></span>

### <span data-ttu-id="1db23-108">Örnek 1: Azure SQL veritabanı için eşitleme grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1db23-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="1db23-109">Bu komut, Azure SQL veritabanı için bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1db23-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="1db23-110">"schema.json" yerel diskteki bir dosyadır.</span><span class="sxs-lookup"><span data-stu-id="1db23-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="1db23-111">JSON biçiminde Shema yükünü içerir.</span><span class="sxs-lookup"><span data-stu-id="1db23-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="1db23-112">JSON şemasının bir örneği: {"tablolar": [{"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}, "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="1db23-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="1db23-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1db23-113">PARAMETERS</span></span>

### <span data-ttu-id="1db23-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1db23-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="1db23-115">Eşitleme grubundaki hub ile üye veritabanı arasında çelişki çözme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="1db23-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="1db23-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="1db23-116">-DatabaseCredential</span></span>
<span data-ttu-id="1db23-117">Hub veritabanının SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1db23-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="1db23-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1db23-118">-DatabaseName</span></span>
<span data-ttu-id="1db23-119">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1db23-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1db23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db23-120">-DefaultProfile</span></span>
<span data-ttu-id="1db23-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1db23-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1db23-122">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="1db23-122">-IntervalInSeconds</span></span>
<span data-ttu-id="1db23-123">Veri eşitlemesinin sıklığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="1db23-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="1db23-124">Varsayılan:-1; Yani otomatik eşitleme etkinleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="1db23-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="1db23-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1db23-125">-Name</span></span>
<span data-ttu-id="1db23-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1db23-126">The sync group name.</span></span>

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

### <span data-ttu-id="1db23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db23-127">-ResourceGroupName</span></span>
<span data-ttu-id="1db23-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1db23-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1db23-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="1db23-129">-SchemaFile</span></span>
<span data-ttu-id="1db23-130">Şema dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="1db23-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="1db23-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1db23-131">-ServerName</span></span>
<span data-ttu-id="1db23-132">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="1db23-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1db23-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1db23-133">-SyncDatabaseName</span></span>
<span data-ttu-id="1db23-134">Eşitleme ile ilgili meta verileri depolamak için kullanılan veritabanı.</span><span class="sxs-lookup"><span data-stu-id="1db23-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="1db23-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db23-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="1db23-136">Eşitleme meta veri veritabanının ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1db23-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="1db23-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="1db23-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="1db23-138">Eşitleme meta veri veritabanının barındırıldığı sunucu.</span><span class="sxs-lookup"><span data-stu-id="1db23-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="1db23-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="1db23-139">-Confirm</span></span>
<span data-ttu-id="1db23-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1db23-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db23-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db23-141">-WhatIf</span></span>
<span data-ttu-id="1db23-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1db23-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db23-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1db23-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db23-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db23-144">CommonParameters</span></span>
<span data-ttu-id="1db23-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1db23-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db23-146">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1db23-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db23-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1db23-147">INPUTS</span></span>

### <span data-ttu-id="1db23-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1db23-148">System.String</span></span>

## <span data-ttu-id="1db23-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1db23-149">OUTPUTS</span></span>

### <span data-ttu-id="1db23-150">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="1db23-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1db23-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1db23-151">NOTES</span></span>

## <span data-ttu-id="1db23-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1db23-152">RELATED LINKS</span></span>

[<span data-ttu-id="1db23-153">Set-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1db23-153">Set-AzSqlSyncGroup</span></span>](./Set-AzSqlSyncGroup.md)

[<span data-ttu-id="1db23-154">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1db23-154">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="1db23-155">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1db23-155">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

