---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: a779217b67cc73f25223661ae8671b4588a8cd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591294"
---
# <span data-ttu-id="6b6a3-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6b6a3-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="6b6a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6a3-103">Azure SQL veritabanı eşitleme üyesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b6a3-104">SYNTAX</span></span>

### <span data-ttu-id="6b6a3-105">Azuressqlveritabanı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b6a3-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b6a3-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="6b6a3-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b6a3-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="6b6a3-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b6a3-108">DESCRIPTION</span></span>
<span data-ttu-id="6b6a3-109">**New-AzureRmSqlSyncMember** cmdlet 'ı BIR Azure SQL veritabanı eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6b6a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b6a3-110">EXAMPLES</span></span>

### <span data-ttu-id="6b6a3-111">Örnek 1: Azure SQL veritabanı için eşitleme üyesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="6b6a3-112">Bu komut, Azure SQL veritabanı için eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="6b6a3-113">Örnek 2: şirket içi bir SQL Server veritabanı için eşitleme üyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b6a3-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="6b6a3-114">Bu komut, şirket içi bir SQL veritabanı için eşitleme üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="6b6a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b6a3-115">PARAMETERS</span></span>

### <span data-ttu-id="6b6a3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-116">-DatabaseName</span></span>
<span data-ttu-id="6b6a3-117">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6b6a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6a3-118">-DefaultProfile</span></span>
<span data-ttu-id="6b6a3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6b6a3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b6a3-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6b6a3-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="6b6a3-121">Azure SQL veritabanının kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="6b6a3-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6b6a3-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-122">-MemberDatabaseName</span></span>
<span data-ttu-id="6b6a3-123">Üye veritabanının Azure SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="6b6a3-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="6b6a3-124">-MemberDatabaseType</span></span>
<span data-ttu-id="6b6a3-125">Üye veritabanının veritabanı türü.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="6b6a3-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-126">-MemberServerName</span></span>
<span data-ttu-id="6b6a3-127">Üye veritabanının Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="6b6a3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b6a3-128">-Name</span></span>
<span data-ttu-id="6b6a3-129">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-129">The sync member name.</span></span>

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

### <span data-ttu-id="6b6a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b6a3-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b6a3-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-132">-ServerName</span></span>
<span data-ttu-id="6b6a3-133">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6b6a3-134">-Sqlserverdatabaseıd</span><span class="sxs-lookup"><span data-stu-id="6b6a3-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="6b6a3-135">Eşitleme Aracısı tarafından Bağlanılan SQL Server veritabanının kimliği.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="6b6a3-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-136">-SyncAgentName</span></span>
<span data-ttu-id="6b6a3-137">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="6b6a3-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="6b6a3-139">Eşitleme aracısının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="6b6a3-140">-Syncagentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6b6a3-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="6b6a3-141">Eşitleme aracısının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="6b6a3-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-142">-SyncAgentServerName</span></span>
<span data-ttu-id="6b6a3-143">Eşitleme aracısının altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="6b6a3-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="6b6a3-144">-SyncDirection</span></span>
<span data-ttu-id="6b6a3-145">Bu eşitleme üyesinin eşitleme yönü.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="6b6a3-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6a3-146">-SyncGroupName</span></span>
<span data-ttu-id="6b6a3-147">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-147">The sync group name.</span></span>

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

### <span data-ttu-id="6b6a3-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b6a3-148">-Confirm</span></span>
<span data-ttu-id="6b6a3-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6a3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6a3-150">-WhatIf</span></span>
<span data-ttu-id="6b6a3-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6a3-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6a3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6a3-153">CommonParameters</span></span>
<span data-ttu-id="6b6a3-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b6a3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6a3-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6a3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6a3-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b6a3-156">INPUTS</span></span>

### <span data-ttu-id="6b6a3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="6b6a3-157">System.String</span></span>

## <span data-ttu-id="6b6a3-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b6a3-158">OUTPUTS</span></span>

### <span data-ttu-id="6b6a3-159">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="6b6a3-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6b6a3-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b6a3-160">NOTES</span></span>

## <span data-ttu-id="6b6a3-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b6a3-161">RELATED LINKS</span></span>

[<span data-ttu-id="6b6a3-162">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6b6a3-162">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="6b6a3-163">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6b6a3-163">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="6b6a3-164">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6b6a3-164">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)
