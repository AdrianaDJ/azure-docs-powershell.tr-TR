---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 708b010a8ff7b2a289d538a07e7b679fcec6efab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764100"
---
# <span data-ttu-id="debc4-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="debc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="debc4-102">SYNOPSIS</span></span>
<span data-ttu-id="debc4-103">Azure SQL veritabanı yük devretme grubunun yük devretmesini yürütür.</span><span class="sxs-lookup"><span data-stu-id="debc4-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="debc4-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="debc4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="debc4-105">DESCRIPTION</span></span>
<span data-ttu-id="debc4-106">Bu komut, bir yük devretme grubundaki sunucuların rollerini değiştirir ve tüm ikincil veritabanlarını birincil role geçirir.</span><span class="sxs-lookup"><span data-stu-id="debc4-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="debc4-107">DNS istemci önbelleği yenilendikten sonra tüm yeni TDS oturumları ikincil sunucuya otomatik olarak yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="debc4-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="debc4-108">Özgün birincil sunucu tekrar çevrimiçi olduğunda, tüm eski birincil veritabanları ikincil role geçer.</span><span class="sxs-lookup"><span data-stu-id="debc4-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="debc4-109">Bu komutu yürütmek için yük devretme grubunun ikincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="debc4-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="debc4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="debc4-110">EXAMPLES</span></span>

### <span data-ttu-id="debc4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="debc4-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="debc4-112">Yük devretme grubunda boru tarafından veri kaybına olanak sağlayan bir yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="debc4-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="debc4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="debc4-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="debc4-114">Verileri kaybetmeden ya da başarısız olacak ve geri dönecek bir en iyi yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="debc4-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="debc4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="debc4-115">PARAMETERS</span></span>

### <span data-ttu-id="debc4-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="debc4-116">-AllowDataLoss</span></span>
<span data-ttu-id="debc4-117">Bunu yapmasanız da veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="debc4-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="debc4-118">Bu, birincil veritabanı kullanılamaz olsa bile yük devretmenin devam etmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="debc4-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="debc4-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="debc4-119">-AsJob</span></span>
<span data-ttu-id="debc4-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="debc4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="debc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debc4-121">-DefaultProfile</span></span>
<span data-ttu-id="debc4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="debc4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="debc4-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="debc4-123">-FailoverGroupName</span></span>
<span data-ttu-id="debc4-124">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="debc4-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="debc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="debc4-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="debc4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="debc4-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="debc4-127">-ServerName</span></span>
<span data-ttu-id="debc4-128">Yük devretme grubunun ikincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="debc4-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="debc4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="debc4-129">-Confirm</span></span>
<span data-ttu-id="debc4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="debc4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="debc4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debc4-131">-WhatIf</span></span>
<span data-ttu-id="debc4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="debc4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="debc4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="debc4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="debc4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debc4-134">CommonParameters</span></span>
<span data-ttu-id="debc4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="debc4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debc4-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debc4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debc4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="debc4-137">INPUTS</span></span>

### <span data-ttu-id="debc4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="debc4-138">System.String</span></span>

## <span data-ttu-id="debc4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="debc4-139">OUTPUTS</span></span>

### <span data-ttu-id="debc4-140">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="debc4-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="debc4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="debc4-141">NOTES</span></span>

## <span data-ttu-id="debc4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="debc4-142">RELATED LINKS</span></span>

[<span data-ttu-id="debc4-143">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="debc4-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="debc4-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="debc4-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="debc4-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="debc4-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="debc4-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="debc4-149">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="debc4-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
