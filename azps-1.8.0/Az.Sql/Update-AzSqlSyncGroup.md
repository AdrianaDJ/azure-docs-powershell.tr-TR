---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 66e03a171e0140dc9f84ad0a9161bf0af5af9b4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758711"
---
# <span data-ttu-id="fa54a-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa54a-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fa54a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa54a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa54a-103">Azure SQL veritabanı eşitleme grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fa54a-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fa54a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa54a-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa54a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa54a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa54a-106">**Update-AzSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fa54a-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fa54a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa54a-107">EXAMPLES</span></span>

### <span data-ttu-id="fa54a-108">Örnek 1: Azure SQL veritabanı için eşitleme grubunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="fa54a-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="fa54a-109">Bu komut, Azure SQL veritabanı için bir eşitleme grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fa54a-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="fa54a-110">"schema.json" yerel diskteki bir dosyadır.</span><span class="sxs-lookup"><span data-stu-id="fa54a-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="fa54a-111">JSON biçiminde Shema yükünü içerir.</span><span class="sxs-lookup"><span data-stu-id="fa54a-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="fa54a-112">JSON şemasının bir örneği: {"tablolar": [{"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"sütunlar": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}, "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="fa54a-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="fa54a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa54a-113">PARAMETERS</span></span>

### <span data-ttu-id="fa54a-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="fa54a-114">-DatabaseCredential</span></span>
<span data-ttu-id="fa54a-115">Hub veritabanının SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="fa54a-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="fa54a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa54a-116">-DatabaseName</span></span>
<span data-ttu-id="fa54a-117">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="fa54a-117">SQL Database name.</span></span>

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

### <span data-ttu-id="fa54a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa54a-118">-DefaultProfile</span></span>
<span data-ttu-id="fa54a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa54a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa54a-120">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="fa54a-120">-IntervalInSeconds</span></span>
<span data-ttu-id="fa54a-121">Veri eşitlemesinin sıklığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="fa54a-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="fa54a-122">Varsayılan:-1; Yani otomatik eşitleme etkinleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="fa54a-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="fa54a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa54a-123">-Name</span></span>
<span data-ttu-id="fa54a-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fa54a-124">The sync group name.</span></span>

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

### <span data-ttu-id="fa54a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa54a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa54a-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fa54a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa54a-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="fa54a-127">-SchemaFile</span></span>
<span data-ttu-id="fa54a-128">Şema dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="fa54a-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="fa54a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa54a-129">-ServerName</span></span>
<span data-ttu-id="fa54a-130">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="fa54a-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fa54a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa54a-131">-Confirm</span></span>
<span data-ttu-id="fa54a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa54a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa54a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa54a-133">-WhatIf</span></span>
<span data-ttu-id="fa54a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa54a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa54a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa54a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa54a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa54a-136">CommonParameters</span></span>
<span data-ttu-id="fa54a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa54a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa54a-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fa54a-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa54a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa54a-139">INPUTS</span></span>

### <span data-ttu-id="fa54a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fa54a-140">System.String</span></span>

## <span data-ttu-id="fa54a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa54a-141">OUTPUTS</span></span>

### <span data-ttu-id="fa54a-142">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="fa54a-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fa54a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa54a-143">NOTES</span></span>

## <span data-ttu-id="fa54a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa54a-144">RELATED LINKS</span></span>

[<span data-ttu-id="fa54a-145">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa54a-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fa54a-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa54a-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="fa54a-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa54a-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

