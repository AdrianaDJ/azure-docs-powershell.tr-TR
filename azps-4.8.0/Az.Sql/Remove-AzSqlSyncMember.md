---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110231"
---
# <span data-ttu-id="42e82-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="42e82-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="42e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e82-102">SYNOPSIS</span></span>
<span data-ttu-id="42e82-103">Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e82-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="42e82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42e82-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42e82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42e82-105">DESCRIPTION</span></span>
<span data-ttu-id="42e82-106">**Remove-AzSqlSyncMember** cmdlet 'ı BIR Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e82-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="42e82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42e82-107">EXAMPLES</span></span>

### <span data-ttu-id="42e82-108">Örnek 1: eşitleme üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="42e82-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="42e82-109">Bu komut, syncMember01 adındaki Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e82-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="42e82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42e82-110">PARAMETERS</span></span>

### <span data-ttu-id="42e82-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42e82-111">-DatabaseName</span></span>
<span data-ttu-id="42e82-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="42e82-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="42e82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e82-113">-DefaultProfile</span></span>
<span data-ttu-id="42e82-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42e82-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42e82-115">-Force</span><span class="sxs-lookup"><span data-stu-id="42e82-115">-Force</span></span>
<span data-ttu-id="42e82-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="42e82-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e82-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="42e82-117">-Name</span></span>
<span data-ttu-id="42e82-118">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="42e82-118">The sync member name.</span></span>

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

### <span data-ttu-id="42e82-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="42e82-119">-PassThru</span></span>
<span data-ttu-id="42e82-120">Kaldırılan eşitleme üyesini verip vermediğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="42e82-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e82-121">-ResourceGroupName</span></span>
<span data-ttu-id="42e82-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="42e82-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="42e82-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42e82-123">-ServerName</span></span>
<span data-ttu-id="42e82-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="42e82-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="42e82-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="42e82-125">-SyncGroupName</span></span>
<span data-ttu-id="42e82-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42e82-126">The sync group name.</span></span>

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

### <span data-ttu-id="42e82-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="42e82-127">-Confirm</span></span>
<span data-ttu-id="42e82-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42e82-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e82-129">-WhatIf</span></span>
<span data-ttu-id="42e82-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42e82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e82-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42e82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e82-132">CommonParameters</span></span>
<span data-ttu-id="42e82-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42e82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e82-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42e82-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e82-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42e82-135">INPUTS</span></span>

### <span data-ttu-id="42e82-136">System. String</span><span class="sxs-lookup"><span data-stu-id="42e82-136">System.String</span></span>

## <span data-ttu-id="42e82-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42e82-137">OUTPUTS</span></span>

### <span data-ttu-id="42e82-138">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="42e82-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="42e82-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42e82-139">NOTES</span></span>

## <span data-ttu-id="42e82-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42e82-140">RELATED LINKS</span></span>

[<span data-ttu-id="42e82-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="42e82-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="42e82-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="42e82-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="42e82-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="42e82-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

