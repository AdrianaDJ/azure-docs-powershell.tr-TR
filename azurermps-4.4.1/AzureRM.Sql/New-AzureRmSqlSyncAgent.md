---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: e296e338d519537f688085fc5c142e3c12804b0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762051"
---
# <span data-ttu-id="e0eda-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e0eda-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="e0eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0eda-102">SYNOPSIS</span></span>
<span data-ttu-id="e0eda-103">Azure SQL eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0eda-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0eda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0eda-104">SYNTAX</span></span>

### <span data-ttu-id="e0eda-105">SyncDatabaseComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0eda-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0eda-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="e0eda-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0eda-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0eda-107">DESCRIPTION</span></span>
<span data-ttu-id="e0eda-108">**Yeni-AzureRmSqlSyncAgent** cmdlet 'ı Azure SQL eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0eda-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e0eda-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0eda-109">EXAMPLES</span></span>

### <span data-ttu-id="e0eda-110">Örnek 1: Azure SQL Server için eşitleme Aracısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0eda-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
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

<span data-ttu-id="e0eda-111">Bu komut, Azure SQL Server için eşitleme Aracısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0eda-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="e0eda-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0eda-112">PARAMETERS</span></span>

### <span data-ttu-id="e0eda-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0eda-113">-Confirm</span></span>
<span data-ttu-id="e0eda-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0eda-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0eda-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0eda-115">-Name</span></span>
<span data-ttu-id="e0eda-116">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="e0eda-116">The sync agent name.</span></span>

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

### <span data-ttu-id="e0eda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0eda-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0eda-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e0eda-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0eda-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0eda-119">-ServerName</span></span>
<span data-ttu-id="e0eda-120">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="e0eda-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="e0eda-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0eda-121">-SyncDatabaseName</span></span>
<span data-ttu-id="e0eda-122">Eşitleme ile ilgili meta verileri depolamak için kullanılan veritabanı.</span><span class="sxs-lookup"><span data-stu-id="e0eda-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="e0eda-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0eda-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="e0eda-124">Eşitleme meta veri veritabanının ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e0eda-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="e0eda-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="e0eda-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="e0eda-126">Eşitleme meta veri veritabanının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e0eda-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="e0eda-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="e0eda-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="e0eda-128">Eşitleme meta veri veritabanının barındırıldığı sunucu.</span><span class="sxs-lookup"><span data-stu-id="e0eda-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="e0eda-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0eda-129">-WhatIf</span></span>
<span data-ttu-id="e0eda-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0eda-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0eda-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0eda-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0eda-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0eda-132">-DefaultProfile</span></span>
<span data-ttu-id="e0eda-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0eda-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0eda-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0eda-134">CommonParameters</span></span>
<span data-ttu-id="e0eda-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0eda-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0eda-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0eda-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0eda-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0eda-137">INPUTS</span></span>

## <span data-ttu-id="e0eda-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0eda-138">OUTPUTS</span></span>

### <span data-ttu-id="e0eda-139">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="e0eda-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="e0eda-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0eda-140">NOTES</span></span>

## <span data-ttu-id="e0eda-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0eda-141">RELATED LINKS</span></span>

[<span data-ttu-id="e0eda-142">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e0eda-142">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="e0eda-143">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e0eda-143">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

