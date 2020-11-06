---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592871"
---
# <span data-ttu-id="7052e-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7052e-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="7052e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7052e-102">SYNOPSIS</span></span>
<span data-ttu-id="7052e-103">SQL veritabanıyla belirtilen ikincil veritabanı arasında veri çoğaltmayı sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="7052e-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7052e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7052e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7052e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7052e-105">DESCRIPTION</span></span>
<span data-ttu-id="7052e-106">**Remove-AzureRmSqlDatabaseSecondary** cmdlet 'i coğrafi çoğaltma bağlantısını sonlandırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7052e-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="7052e-107">Bu cmdlet Stop-AzureSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7052e-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="7052e-108">İşten çıkmadan önce çoğaltma eşitlemesi yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="7052e-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="7052e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7052e-109">EXAMPLES</span></span>

## <span data-ttu-id="7052e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7052e-110">PARAMETERS</span></span>

### <span data-ttu-id="7052e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7052e-111">-DatabaseName</span></span>
<span data-ttu-id="7052e-112">Bu cmdlet 'in kaldırıldığı çoğaltma bağlantısının bulunduğu birincil Azure SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7052e-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7052e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7052e-113">-DefaultProfile</span></span>
<span data-ttu-id="7052e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7052e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7052e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7052e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7052e-116">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7052e-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="7052e-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="7052e-117">-PartnerServerName</span></span>
<span data-ttu-id="7052e-118">İş ortağı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7052e-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="7052e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7052e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7052e-120">Kaldırılacak olan çoğaltma bağlantısıyla ilişkilendirilmiş olan kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7052e-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="7052e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7052e-121">-ServerName</span></span>
<span data-ttu-id="7052e-122">Kaldırılacak çoğaltma bağlantısının bulunduğu SQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7052e-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="7052e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="7052e-123">-Confirm</span></span>
<span data-ttu-id="7052e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7052e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7052e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7052e-125">-WhatIf</span></span>
<span data-ttu-id="7052e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7052e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7052e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7052e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7052e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7052e-128">CommonParameters</span></span>
<span data-ttu-id="7052e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7052e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7052e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7052e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7052e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7052e-131">INPUTS</span></span>

###  
<span data-ttu-id="7052e-132">Birincil veya ikincil veritabanı için **veritabanı** nesnesinin örneklerini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7052e-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="7052e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7052e-133">OUTPUTS</span></span>

###  
<span data-ttu-id="7052e-134">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7052e-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7052e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7052e-135">NOTES</span></span>

## <span data-ttu-id="7052e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7052e-136">RELATED LINKS</span></span>

[<span data-ttu-id="7052e-137">Yeni-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7052e-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7052e-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7052e-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7052e-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7052e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
