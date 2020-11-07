---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: a8e890bfa9c839c97ddc3d0f002782fdc0b4f2e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933555"
---
# <span data-ttu-id="3c8da-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="3c8da-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="3c8da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c8da-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8da-103">Azure SQL eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c8da-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="3c8da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c8da-104">SYNTAX</span></span>

### <span data-ttu-id="3c8da-105">SyncDatabaseComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c8da-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8da-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="3c8da-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c8da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c8da-107">DESCRIPTION</span></span>
<span data-ttu-id="3c8da-108">**New-AzSqlSyncAgent** cmdlet 'ı Azure SQL eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c8da-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="3c8da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c8da-109">EXAMPLES</span></span>

### <span data-ttu-id="3c8da-110">Örnek 1: Azure SQL Server için eşitleme Aracısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3c8da-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="3c8da-111">Bu komut, Azure SQL Server için eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c8da-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="3c8da-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c8da-112">PARAMETERS</span></span>

### <span data-ttu-id="3c8da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8da-113">-DefaultProfile</span></span>
<span data-ttu-id="3c8da-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3c8da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c8da-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c8da-115">-Name</span></span>
<span data-ttu-id="3c8da-116">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="3c8da-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8da-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c8da-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3c8da-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c8da-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c8da-119">-ServerName</span></span>
<span data-ttu-id="3c8da-120">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="3c8da-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="3c8da-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c8da-121">-SyncDatabaseName</span></span>
<span data-ttu-id="3c8da-122">Eşitleme ile ilgili meta verileri depolamak için kullanılan veritabanı.</span><span class="sxs-lookup"><span data-stu-id="3c8da-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8da-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="3c8da-124">Eşitleme meta veri veritabanının ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3c8da-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="3c8da-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="3c8da-126">Eşitleme meta veri veritabanının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3c8da-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="3c8da-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="3c8da-128">Eşitleme meta veri veritabanının barındırıldığı sunucu.</span><span class="sxs-lookup"><span data-stu-id="3c8da-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c8da-129">-Confirm</span></span>
<span data-ttu-id="3c8da-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c8da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8da-131">-WhatIf</span></span>
<span data-ttu-id="3c8da-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c8da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c8da-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c8da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8da-134">CommonParameters</span></span>
<span data-ttu-id="3c8da-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c8da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8da-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c8da-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8da-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c8da-137">INPUTS</span></span>

### <span data-ttu-id="3c8da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3c8da-138">System.String</span></span>

## <span data-ttu-id="3c8da-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c8da-139">OUTPUTS</span></span>

### <span data-ttu-id="3c8da-140">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="3c8da-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="3c8da-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c8da-141">NOTES</span></span>

## <span data-ttu-id="3c8da-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c8da-142">RELATED LINKS</span></span>

[<span data-ttu-id="3c8da-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="3c8da-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="3c8da-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="3c8da-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

