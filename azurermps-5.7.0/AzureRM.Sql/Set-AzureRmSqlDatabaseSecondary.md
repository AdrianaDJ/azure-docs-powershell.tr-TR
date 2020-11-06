---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588699"
---
# <span data-ttu-id="ee44d-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee44d-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ee44d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee44d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee44d-103">Bir ikincil veritabanını, yük devretmeyi başlatmak için birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee44d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee44d-104">SYNTAX</span></span>

### <span data-ttu-id="ee44d-105">Noseçenekdeğer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee44d-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee44d-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="ee44d-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee44d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee44d-107">DESCRIPTION</span></span>
<span data-ttu-id="ee44d-108">**Set-AzureRmSqlDatabaseSecondary** cmdlet 'i, bir ikincil veritabanını, yük devretmeyi başlatmak için birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="ee44d-109">Bu cmdlet genel yapılandırma komutu olarak tasarlanmıştır, ancak şu anda yük devretmenin başlatılmasına sınırlı.</span><span class="sxs-lookup"><span data-stu-id="ee44d-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="ee44d-110">Kesinti sırasında bir yük devretmeyi zorla başlatmak için *Allowdataloss* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ee44d-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="ee44d-111">Kurtarma detayu gibi bir planlı işlemi gerçekleştirdiğinizde bu parametreyi belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ee44d-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="ee44d-112">İkinci durumda, ikincil veritabanı geçiş yapılmadan önce birincili ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="ee44d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee44d-113">EXAMPLES</span></span>

## <span data-ttu-id="ee44d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee44d-114">PARAMETERS</span></span>

### <span data-ttu-id="ee44d-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ee44d-115">-AllowDataLoss</span></span>
<span data-ttu-id="ee44d-116">Bu yük devretme işleminin veri kaybına izin verdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="ee44d-117">-AsJob</span></span>
<span data-ttu-id="ee44d-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ee44d-118">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee44d-119">-DatabaseName</span></span>
<span data-ttu-id="ee44d-120">Azure SQL veritabanı Ikincil adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee44d-121">-DefaultProfile</span></span>
<span data-ttu-id="ee44d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee44d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-123">-Yük devretme</span><span class="sxs-lookup"><span data-stu-id="ee44d-123">-Failover</span></span>
<span data-ttu-id="ee44d-124">Bu işlemin bir yük devretme olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee44d-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ee44d-126">İş ortağı Azure SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee44d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee44d-128">Azure SQL veritabanı Ikincili 'nin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee44d-129">-ServerName</span></span>
<span data-ttu-id="ee44d-130">Azure SQL veritabanı Secondary 'i barındıran SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee44d-131">-Confirm</span></span>
<span data-ttu-id="ee44d-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee44d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee44d-133">-WhatIf</span></span>
<span data-ttu-id="ee44d-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee44d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee44d-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee44d-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee44d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee44d-136">CommonParameters</span></span>
<span data-ttu-id="ee44d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee44d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee44d-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee44d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee44d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee44d-139">INPUTS</span></span>

###  
<span data-ttu-id="ee44d-140">İkincil veritabanının **veritabanı** nesnesinin örneklerini yük devri ve birincil veritabanını bu cmdlet 'e yapmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee44d-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="ee44d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee44d-141">OUTPUTS</span></span>

###  
<span data-ttu-id="ee44d-142">Bu cmdlet bir **Replicationlink** döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee44d-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="ee44d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee44d-143">NOTES</span></span>

## <span data-ttu-id="ee44d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee44d-144">RELATED LINKS</span></span>

[<span data-ttu-id="ee44d-145">Yeni-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee44d-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ee44d-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee44d-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ee44d-147">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ee44d-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
