---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 34aec11e5f4bd2ee0aef37a4287544081bb9a87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592166"
---
# <span data-ttu-id="b3762-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="b3762-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="b3762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3762-102">SYNOPSIS</span></span>
<span data-ttu-id="b3762-103">Eşitleme şemasını bir eşitleme üyesi veritabanı veya Eşitleme Merkezi veritabanı için güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b3762-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="b3762-104">Gerçek veritabanından en son veritabanı şemasını alır ve sonra da bunu kullanarak, eşitleme meta verileri veritabanı tarafından önbelleğe alınan şemayı yeniler.</span><span class="sxs-lookup"><span data-stu-id="b3762-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="b3762-105">"SyncMemberName" belirtilirse, üye veritabanı şemasını yeniler; yoksa, hub veritabanı şemasını yeniler.</span><span class="sxs-lookup"><span data-stu-id="b3762-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3762-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3762-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3762-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3762-107">DESCRIPTION</span></span>
<span data-ttu-id="b3762-108">**Update-AzureRmSqlSyncSchema** cmdlet 'i, eşitleme şemasını bir eşitleme üyesi veritabanı veya Eşitleme Merkezi veritabanı için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b3762-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="b3762-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3762-109">EXAMPLES</span></span>

### <span data-ttu-id="b3762-110">Örnek 1: hub veritabanı için eşitleme şemasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b3762-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="b3762-111">Bu komut, eşitleme grubundaki hub veritabanı için eşitleme şemasını syncGroup01</span><span class="sxs-lookup"><span data-stu-id="b3762-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="b3762-112">Örnek 2: bir üye veritabanı için eşitleme şemasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b3762-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="b3762-113">Bu komut, eşitleme üyesinde üye veritabanı için eşitleme şemasını syncMember01</span><span class="sxs-lookup"><span data-stu-id="b3762-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="b3762-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3762-114">PARAMETERS</span></span>

### <span data-ttu-id="b3762-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3762-115">-Confirm</span></span>
<span data-ttu-id="b3762-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3762-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3762-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3762-117">-DatabaseName</span></span>
<span data-ttu-id="b3762-118">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="b3762-118">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b3762-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b3762-119">-PassThru</span></span>
<span data-ttu-id="b3762-120">Bu cmdlet 'in çalışma</span><span class="sxs-lookup"><span data-stu-id="b3762-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="b3762-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3762-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3762-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b3762-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b3762-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3762-123">-ServerName</span></span>
<span data-ttu-id="b3762-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="b3762-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b3762-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b3762-125">-SyncGroupName</span></span>
<span data-ttu-id="b3762-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b3762-126">The sync group name.</span></span>

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

### <span data-ttu-id="b3762-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="b3762-127">-SyncMemberName</span></span>
<span data-ttu-id="b3762-128">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="b3762-128">The sync member name.</span></span>

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

### <span data-ttu-id="b3762-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3762-129">-WhatIf</span></span>
<span data-ttu-id="b3762-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3762-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3762-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3762-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3762-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3762-132">-DefaultProfile</span></span>
<span data-ttu-id="b3762-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3762-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3762-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3762-134">CommonParameters</span></span>
<span data-ttu-id="b3762-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3762-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3762-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3762-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3762-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3762-137">INPUTS</span></span>

## <span data-ttu-id="b3762-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3762-138">OUTPUTS</span></span>

### <span data-ttu-id="b3762-139">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="b3762-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b3762-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3762-140">NOTES</span></span>

## <span data-ttu-id="b3762-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3762-141">RELATED LINKS</span></span>

