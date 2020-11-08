---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275649"
---
# <span data-ttu-id="6bb06-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6bb06-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="6bb06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb06-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb06-103">Bir ikincil veritabanını, yük devretmeyi başlatmak için birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="6bb06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bb06-104">SYNTAX</span></span>

### <span data-ttu-id="6bb06-105">Noseçenekdeğer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bb06-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb06-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="6bb06-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb06-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bb06-107">DESCRIPTION</span></span>
<span data-ttu-id="6bb06-108">**Set-AzSqlDatabaseSecondary** cmdlet 'i, yük devretmeyi başlatmak için ikincil bir veritabanını birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="6bb06-109">Bu cmdlet genel yapılandırma komutu olarak tasarlanmıştır, ancak şu anda yük devretmenin başlatılmasına sınırlı.</span><span class="sxs-lookup"><span data-stu-id="6bb06-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="6bb06-110">Kesinti sırasında bir yük devretmeyi zorla başlatmak için *Allowdataloss* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6bb06-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="6bb06-111">Kurtarma detayu gibi bir planlı işlemi gerçekleştirdiğinizde bu parametreyi belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="6bb06-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="6bb06-112">İkinci durumda, ikincil veritabanı geçiş yapılmadan önce birincili ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="6bb06-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bb06-113">EXAMPLES</span></span>

### <span data-ttu-id="6bb06-114">Örnek 1: planlı bir yük devretme başlatma</span><span class="sxs-lookup"><span data-stu-id="6bb06-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="6bb06-115">Örnek 2: Zorlanmış yük devretme başlatma (olası veri kaybıyla)</span><span class="sxs-lookup"><span data-stu-id="6bb06-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="6bb06-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bb06-116">PARAMETERS</span></span>

### <span data-ttu-id="6bb06-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6bb06-117">-AllowDataLoss</span></span>
<span data-ttu-id="6bb06-118">Bu yük devretme işleminin veri kaybına izin verdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb06-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="6bb06-119">-AsJob</span></span>
<span data-ttu-id="6bb06-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6bb06-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bb06-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6bb06-121">-DatabaseName</span></span>
<span data-ttu-id="6bb06-122">Azure SQL veritabanı Ikincil adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="6bb06-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb06-123">-DefaultProfile</span></span>
<span data-ttu-id="6bb06-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6bb06-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bb06-125">-Yük devretme</span><span class="sxs-lookup"><span data-stu-id="6bb06-125">-Failover</span></span>
<span data-ttu-id="6bb06-126">Bu işlemin bir yük devretme olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb06-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb06-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6bb06-128">İş ortağı Azure SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb06-129">-ResourceGroupName</span></span>
<span data-ttu-id="6bb06-130">Azure SQL veritabanı Ikincili 'nin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="6bb06-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6bb06-131">-ServerName</span></span>
<span data-ttu-id="6bb06-132">Azure SQL veritabanı Secondary 'i barındıran SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="6bb06-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bb06-133">-Confirm</span></span>
<span data-ttu-id="6bb06-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bb06-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb06-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb06-135">-WhatIf</span></span>
<span data-ttu-id="6bb06-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bb06-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb06-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bb06-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb06-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb06-138">CommonParameters</span></span>
<span data-ttu-id="6bb06-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bb06-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb06-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6bb06-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb06-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bb06-141">INPUTS</span></span>

### <span data-ttu-id="6bb06-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6bb06-142">System.String</span></span>

## <span data-ttu-id="6bb06-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bb06-143">OUTPUTS</span></span>

### <span data-ttu-id="6bb06-144">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="6bb06-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="6bb06-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bb06-145">NOTES</span></span>

## <span data-ttu-id="6bb06-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bb06-146">RELATED LINKS</span></span>

[<span data-ttu-id="6bb06-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6bb06-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6bb06-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6bb06-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6bb06-149">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6bb06-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
