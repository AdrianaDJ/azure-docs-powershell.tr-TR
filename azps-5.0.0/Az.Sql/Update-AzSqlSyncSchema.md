---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325024"
---
# <span data-ttu-id="86aa8-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="86aa8-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="86aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="86aa8-103">Eşitleme şemasını bir eşitleme üyesi veritabanı veya Eşitleme Merkezi veritabanı için güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="86aa8-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="86aa8-104">Gerçek veritabanından en son veritabanı şemasını alır ve sonra da bunu kullanarak, eşitleme meta verileri veritabanı tarafından önbelleğe alınan şemayı yeniler.</span><span class="sxs-lookup"><span data-stu-id="86aa8-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="86aa8-105">"SyncMemberName" belirtilirse, üye veritabanı şemasını yeniler; yoksa, hub veritabanı şemasını yeniler.</span><span class="sxs-lookup"><span data-stu-id="86aa8-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="86aa8-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86aa8-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86aa8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="86aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="86aa8-108">**Update-AzSqlSyncSchema** cmdlet 'i, eşitleme şemasını bir eşitleme üyesi veritabanı veya Eşitleme Merkezi veritabanı için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="86aa8-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="86aa8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="86aa8-110">Örnek 1: hub veritabanı için eşitleme şemasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="86aa8-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="86aa8-111">Bu komut, eşitleme grubundaki hub veritabanı için eşitleme şemasını syncGroup01</span><span class="sxs-lookup"><span data-stu-id="86aa8-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="86aa8-112">Örnek 2: bir üye veritabanı için eşitleme şemasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="86aa8-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="86aa8-113">Bu komut, eşitleme üyesinde üye veritabanı için eşitleme şemasını syncMember01</span><span class="sxs-lookup"><span data-stu-id="86aa8-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="86aa8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="86aa8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86aa8-115">-DatabaseName</span></span>
<span data-ttu-id="86aa8-116">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="86aa8-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="86aa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86aa8-117">-DefaultProfile</span></span>
<span data-ttu-id="86aa8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="86aa8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86aa8-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="86aa8-119">-PassThru</span></span>
<span data-ttu-id="86aa8-120">Bu cmdlet 'in çalışma</span><span class="sxs-lookup"><span data-stu-id="86aa8-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="86aa8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86aa8-121">-ResourceGroupName</span></span>
<span data-ttu-id="86aa8-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="86aa8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="86aa8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86aa8-123">-ServerName</span></span>
<span data-ttu-id="86aa8-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="86aa8-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="86aa8-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="86aa8-125">-SyncGroupName</span></span>
<span data-ttu-id="86aa8-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="86aa8-126">The sync group name.</span></span>

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

### <span data-ttu-id="86aa8-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="86aa8-127">-SyncMemberName</span></span>
<span data-ttu-id="86aa8-128">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="86aa8-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86aa8-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="86aa8-129">-Confirm</span></span>
<span data-ttu-id="86aa8-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86aa8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86aa8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86aa8-131">-WhatIf</span></span>
<span data-ttu-id="86aa8-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86aa8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86aa8-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86aa8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86aa8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86aa8-134">CommonParameters</span></span>
<span data-ttu-id="86aa8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86aa8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86aa8-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="86aa8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86aa8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86aa8-137">INPUTS</span></span>

### <span data-ttu-id="86aa8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="86aa8-138">System.String</span></span>

## <span data-ttu-id="86aa8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86aa8-139">OUTPUTS</span></span>

### <span data-ttu-id="86aa8-140">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="86aa8-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="86aa8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86aa8-141">NOTES</span></span>

## <span data-ttu-id="86aa8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86aa8-142">RELATED LINKS</span></span>
