---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933994"
---
# <span data-ttu-id="026cc-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="026cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="026cc-102">SYNOPSIS</span></span>
<span data-ttu-id="026cc-103">Azure SQL veritabanı yük devretme grubunun yük devretmesini yürütür.</span><span class="sxs-lookup"><span data-stu-id="026cc-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="026cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="026cc-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="026cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="026cc-105">DESCRIPTION</span></span>
<span data-ttu-id="026cc-106">Bu komut, bir yük devretme grubundaki sunucuların rollerini değiştirir ve tüm ikincil veritabanlarını birincil role geçirir.</span><span class="sxs-lookup"><span data-stu-id="026cc-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="026cc-107">DNS istemci önbelleği yenilendikten sonra tüm yeni TDS oturumları ikincil sunucuya otomatik olarak yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="026cc-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="026cc-108">Özgün birincil sunucu tekrar çevrimiçi olduğunda, tüm eski birincil veritabanları ikincil role geçer.</span><span class="sxs-lookup"><span data-stu-id="026cc-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="026cc-109">Bu komutu yürütmek için yük devretme grubunun ikincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="026cc-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="026cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="026cc-110">EXAMPLES</span></span>

### <span data-ttu-id="026cc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="026cc-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="026cc-112">Yük devretme grubunda boru tarafından veri kaybına olanak sağlayan bir yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="026cc-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="026cc-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="026cc-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="026cc-114">Verileri kaybetmeden ya da başarısız olacak ve geri dönecek bir en iyi yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="026cc-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="026cc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="026cc-115">PARAMETERS</span></span>

### <span data-ttu-id="026cc-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="026cc-116">-AllowDataLoss</span></span>
<span data-ttu-id="026cc-117">Bunu yapmasanız da veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="026cc-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="026cc-118">Bu, birincil veritabanı kullanılamaz olsa bile yük devretmenin devam etmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="026cc-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="026cc-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="026cc-119">-AsJob</span></span>
<span data-ttu-id="026cc-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="026cc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="026cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026cc-121">-DefaultProfile</span></span>
<span data-ttu-id="026cc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="026cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="026cc-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="026cc-123">-FailoverGroupName</span></span>
<span data-ttu-id="026cc-124">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="026cc-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="026cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="026cc-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="026cc-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="026cc-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="026cc-127">-ServerName</span></span>
<span data-ttu-id="026cc-128">Yük devretme grubunun ikincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="026cc-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="026cc-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="026cc-129">-Confirm</span></span>
<span data-ttu-id="026cc-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="026cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="026cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="026cc-131">-WhatIf</span></span>
<span data-ttu-id="026cc-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="026cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="026cc-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="026cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="026cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026cc-134">CommonParameters</span></span>
<span data-ttu-id="026cc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="026cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026cc-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="026cc-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026cc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="026cc-137">INPUTS</span></span>

### <span data-ttu-id="026cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="026cc-138">System.String</span></span>

## <span data-ttu-id="026cc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="026cc-139">OUTPUTS</span></span>

### <span data-ttu-id="026cc-140">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="026cc-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="026cc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="026cc-141">NOTES</span></span>

## <span data-ttu-id="026cc-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="026cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="026cc-143">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="026cc-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="026cc-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="026cc-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="026cc-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="026cc-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="026cc-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="026cc-149">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="026cc-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
