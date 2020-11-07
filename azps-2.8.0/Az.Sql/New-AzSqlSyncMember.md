---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933824"
---
# <span data-ttu-id="7f548-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7f548-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="7f548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f548-102">SYNOPSIS</span></span>
<span data-ttu-id="7f548-103">Azure SQL veritabanı eşitleme üyesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f548-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7f548-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f548-104">SYNTAX</span></span>

### <span data-ttu-id="7f548-105">Azuressqlveritabanı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f548-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f548-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="7f548-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f548-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="7f548-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f548-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f548-108">DESCRIPTION</span></span>
<span data-ttu-id="7f548-109">**New-AzSqlSyncMember** cmdlet 'ı BIR Azure SQL veritabanı eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f548-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7f548-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f548-110">EXAMPLES</span></span>

### <span data-ttu-id="7f548-111">Örnek 1: Azure SQL veritabanı için eşitleme üyesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7f548-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="7f548-112">Bu komut, Azure SQL veritabanı için eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f548-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="7f548-113">Örnek 2: şirket içi bir SQL Server veritabanı için eşitleme üyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f548-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="7f548-114">Bu komut, şirket içi bir SQL veritabanı için eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f548-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="7f548-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f548-115">PARAMETERS</span></span>

### <span data-ttu-id="7f548-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f548-116">-DatabaseName</span></span>
<span data-ttu-id="7f548-117">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7f548-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f548-118">-DefaultProfile</span></span>
<span data-ttu-id="7f548-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f548-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f548-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7f548-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="7f548-121">Azure SQL veritabanının kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="7f548-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f548-122">-MemberDatabaseName</span></span>
<span data-ttu-id="7f548-123">Üye veritabanının Azure SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="7f548-124">-MemberDatabaseType</span></span>
<span data-ttu-id="7f548-125">Üye veritabanının veritabanı türü.</span><span class="sxs-lookup"><span data-stu-id="7f548-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="7f548-126">-MemberServerName</span></span>
<span data-ttu-id="7f548-127">Üye veritabanının Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f548-128">-Name</span></span>
<span data-ttu-id="7f548-129">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f548-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f548-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f548-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f548-132">-ServerName</span></span>
<span data-ttu-id="7f548-133">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7f548-134">-Sqlserverdatabaseıd</span><span class="sxs-lookup"><span data-stu-id="7f548-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="7f548-135">Eşitleme Aracısı tarafından Bağlanılan SQL Server veritabanının kimliği.</span><span class="sxs-lookup"><span data-stu-id="7f548-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="7f548-136">-SyncAgentName</span></span>
<span data-ttu-id="7f548-137">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f548-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="7f548-139">Eşitleme aracısının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-140">-Syncagentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7f548-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="7f548-141">Eşitleme aracısının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7f548-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="7f548-142">-SyncAgentServerName</span></span>
<span data-ttu-id="7f548-143">Eşitleme aracısının altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="7f548-144">-SyncDirection</span></span>
<span data-ttu-id="7f548-145">Bu eşitleme üyesinin eşitleme yönü.</span><span class="sxs-lookup"><span data-stu-id="7f548-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7f548-146">-SyncGroupName</span></span>
<span data-ttu-id="7f548-147">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7f548-147">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f548-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f548-148">-Confirm</span></span>
<span data-ttu-id="7f548-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f548-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f548-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f548-150">-WhatIf</span></span>
<span data-ttu-id="7f548-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f548-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f548-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f548-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f548-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f548-153">CommonParameters</span></span>
<span data-ttu-id="7f548-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f548-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f548-155">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f548-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f548-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f548-156">INPUTS</span></span>

### <span data-ttu-id="7f548-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7f548-157">System.String</span></span>

## <span data-ttu-id="7f548-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f548-158">OUTPUTS</span></span>

### <span data-ttu-id="7f548-159">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="7f548-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="7f548-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f548-160">NOTES</span></span>

## <span data-ttu-id="7f548-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f548-161">RELATED LINKS</span></span>

[<span data-ttu-id="7f548-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7f548-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="7f548-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7f548-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="7f548-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7f548-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

