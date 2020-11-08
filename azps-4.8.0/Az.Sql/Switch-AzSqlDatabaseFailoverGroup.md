---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 08192eb96b7c0a2dde84a51cf49f3b96e5429ffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2020
ms.locfileid: "94275128"
---
# <span data-ttu-id="6a047-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="6a047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a047-102">SYNOPSIS</span></span>
<span data-ttu-id="6a047-103">Azure SQL veritabanı yük devretme grubunun yük devretmesini yürütür.</span><span class="sxs-lookup"><span data-stu-id="6a047-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6a047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a047-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a047-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a047-105">DESCRIPTION</span></span>
<span data-ttu-id="6a047-106">Bu komut, bir yük devretme grubundaki sunucuların rollerini değiştirir ve tüm ikincil veritabanlarını birincil role geçirir.</span><span class="sxs-lookup"><span data-stu-id="6a047-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="6a047-107">DNS istemci önbelleği yenilendikten sonra tüm yeni TDS oturumları ikincil sunucuya otomatik olarak yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="6a047-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="6a047-108">Özgün birincil sunucu tekrar çevrimiçi olduğunda, tüm eski birincil veritabanları ikincil role geçer.</span><span class="sxs-lookup"><span data-stu-id="6a047-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="6a047-109">Bu komutu yürütmek için yük devretme grubunun ikincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6a047-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="6a047-110">AllowDataLoss parametresi belirtilmemişse, bu komut her iki rol de değiştirilene kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="6a047-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="6a047-111">AllowDataLoss parametresi belirtilmişse, komut yalnızca yeni birincil öğenin rolünü varsayana kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="6a047-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="6a047-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a047-112">EXAMPLES</span></span>

### <span data-ttu-id="6a047-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a047-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="6a047-114">Yük devretme grubunda boru tarafından veri kaybına olanak sağlayan bir yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="6a047-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="6a047-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6a047-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="6a047-116">Verileri kaybetmeden ya da başarısız olacak ve geri dönecek bir en iyi yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="6a047-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="6a047-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a047-117">PARAMETERS</span></span>

### <span data-ttu-id="6a047-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6a047-118">-AllowDataLoss</span></span>
<span data-ttu-id="6a047-119">Bunu yapmasanız da veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="6a047-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="6a047-120">Bu, birincil veritabanı kullanılamaz olsa bile yük devretmenin devam etmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6a047-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a047-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="6a047-121">-AsJob</span></span>
<span data-ttu-id="6a047-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6a047-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a047-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a047-123">-DefaultProfile</span></span>
<span data-ttu-id="6a047-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6a047-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a047-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6a047-125">-FailoverGroupName</span></span>
<span data-ttu-id="6a047-126">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a047-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a047-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a047-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a047-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a047-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a047-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a047-129">-ServerName</span></span>
<span data-ttu-id="6a047-130">Yük devretme grubunun ikincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a047-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="6a047-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a047-131">-Confirm</span></span>
<span data-ttu-id="6a047-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a047-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a047-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a047-133">-WhatIf</span></span>
<span data-ttu-id="6a047-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a047-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a047-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a047-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a047-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a047-136">CommonParameters</span></span>
<span data-ttu-id="6a047-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a047-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a047-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a047-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a047-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a047-139">INPUTS</span></span>

### <span data-ttu-id="6a047-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6a047-140">System.String</span></span>

## <span data-ttu-id="6a047-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a047-141">OUTPUTS</span></span>

### <span data-ttu-id="6a047-142">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="6a047-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6a047-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a047-143">NOTES</span></span>

## <span data-ttu-id="6a047-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a047-144">RELATED LINKS</span></span>

[<span data-ttu-id="6a047-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6a047-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6a047-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6a047-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="6a047-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6a047-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6a047-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6a047-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6a047-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
