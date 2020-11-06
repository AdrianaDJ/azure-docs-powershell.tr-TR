---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589033"
---
# <span data-ttu-id="b3c9a-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3c9a-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b3c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c9a-103">Bir ikincil veritabanını, yük devretmeyi başlatmak için birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3c9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3c9a-104">SYNTAX</span></span>

### <span data-ttu-id="b3c9a-105">Noseçenekdeğer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3c9a-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3c9a-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="b3c9a-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3c9a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3c9a-107">DESCRIPTION</span></span>
<span data-ttu-id="b3c9a-108">**Set-AzureRmSqlDatabaseSecondary** cmdlet 'i, bir ikincil veritabanını, yük devretmeyi başlatmak için birincil olacak şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="b3c9a-109">Bu cmdlet genel yapılandırma komutu olarak tasarlanmıştır, ancak şu anda yük devretmenin başlatılmasına sınırlı.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="b3c9a-110">Kesinti sırasında bir yük devretmeyi zorla başlatmak için *Allowdataloss* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="b3c9a-111">Kurtarma detayu gibi bir planlı işlemi gerçekleştirdiğinizde bu parametreyi belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="b3c9a-112">İkinci durumda, ikincil veritabanı geçiş yapılmadan önce birincili ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="b3c9a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3c9a-113">EXAMPLES</span></span>

## <span data-ttu-id="b3c9a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3c9a-114">PARAMETERS</span></span>

### <span data-ttu-id="b3c9a-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b3c9a-115">-AllowDataLoss</span></span>
<span data-ttu-id="b3c9a-116">Bu yük devretme işleminin veri kaybına izin verdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="b3c9a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3c9a-117">-DatabaseName</span></span>
<span data-ttu-id="b3c9a-118">Azure SQL veritabanı Ikincil adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-118">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b3c9a-119">-Yük devretme</span><span class="sxs-lookup"><span data-stu-id="b3c9a-119">-Failover</span></span>
<span data-ttu-id="b3c9a-120">Bu işlemin bir yük devretme olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-120">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="b3c9a-121">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c9a-121">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b3c9a-122">İş ortağı Azure SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-122">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b3c9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3c9a-124">Azure SQL veritabanı Ikincili 'nin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-124">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="b3c9a-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3c9a-125">-ServerName</span></span>
<span data-ttu-id="b3c9a-126">Azure SQL veritabanı Secondary 'i barındıran SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-126">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b3c9a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3c9a-127">-Confirm</span></span>
<span data-ttu-id="b3c9a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c9a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c9a-129">-WhatIf</span></span>
<span data-ttu-id="b3c9a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3c9a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c9a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c9a-132">-DefaultProfile</span></span>
<span data-ttu-id="b3c9a-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3c9a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c9a-134">CommonParameters</span></span>
<span data-ttu-id="b3c9a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c9a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c9a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c9a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3c9a-137">INPUTS</span></span>

###  
<span data-ttu-id="b3c9a-138">İkincil veritabanının **veritabanı** nesnesinin örneklerini yük devri ve birincil veritabanını bu cmdlet 'e yapmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-138">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="b3c9a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3c9a-139">OUTPUTS</span></span>

###  
<span data-ttu-id="b3c9a-140">Bu cmdlet bir **Replicationlink** döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-140">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="b3c9a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3c9a-141">NOTES</span></span>

## <span data-ttu-id="b3c9a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3c9a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b3c9a-143">Yeni-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3c9a-143">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b3c9a-144">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3c9a-144">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b3c9a-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b3c9a-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
