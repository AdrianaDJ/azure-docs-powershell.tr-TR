---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096236"
---
# <span data-ttu-id="316c6-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="316c6-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="316c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316c6-102">SYNOPSIS</span></span>
<span data-ttu-id="316c6-103">Bir veritabanını yerine ekleme.</span><span class="sxs-lookup"><span data-stu-id="316c6-103">Failovers a database.</span></span>

## <span data-ttu-id="316c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="316c6-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="316c6-105">DESCRIPTION</span></span>
<span data-ttu-id="316c6-106">Invoke-AzSqlDatabaseFailover cmdlet 'i Azure SQL veritabanı 'nı kullanın.</span><span class="sxs-lookup"><span data-stu-id="316c6-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="316c6-107">Veritabanı elastik bir havuzda ise bu komut, verilen veritabanı aynı elastik havuzda bulunan diğer veritabanlarını etkilemeden yük devretecektir.</span><span class="sxs-lookup"><span data-stu-id="316c6-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="316c6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="316c6-108">EXAMPLES</span></span>

### <span data-ttu-id="316c6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="316c6-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="316c6-110">Bu komut, "Server01" adlı sunucudaki "Database01" adlı veritabanının birincil çoğaltmasının yükünü devreedecek</span><span class="sxs-lookup"><span data-stu-id="316c6-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="316c6-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="316c6-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="316c6-112">Bu komut, "Server01" adlı sunucudaki "Database01" adlı veritabanının</span><span class="sxs-lookup"><span data-stu-id="316c6-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="316c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="316c6-113">PARAMETERS</span></span>

### <span data-ttu-id="316c6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="316c6-114">-AsJob</span></span>
<span data-ttu-id="316c6-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="316c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="316c6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="316c6-116">-DatabaseName</span></span>
<span data-ttu-id="316c6-117">Yük devretmeye yönelik Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="316c6-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="316c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316c6-118">-DefaultProfile</span></span>
<span data-ttu-id="316c6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="316c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316c6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="316c6-120">-Force</span></span>
<span data-ttu-id="316c6-121">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="316c6-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="316c6-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="316c6-122">-PassThru</span></span>
<span data-ttu-id="316c6-123">Başarılı bir yürütmede, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="316c6-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="316c6-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="316c6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="316c6-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="316c6-125">-ReadableSecondary</span></span>
<span data-ttu-id="316c6-126">Yük devretme varsayılan birincil çoğaltma yerine okunabilir ikincil çoğaltma</span><span class="sxs-lookup"><span data-stu-id="316c6-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="316c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="316c6-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="316c6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="316c6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="316c6-129">-ServerName</span></span>
<span data-ttu-id="316c6-130">Veritabanının bulunduğu Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="316c6-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="316c6-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="316c6-131">-Confirm</span></span>
<span data-ttu-id="316c6-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="316c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316c6-133">-WhatIf</span></span>
<span data-ttu-id="316c6-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="316c6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="316c6-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="316c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316c6-136">CommonParameters</span></span>
<span data-ttu-id="316c6-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="316c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316c6-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="316c6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316c6-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="316c6-139">INPUTS</span></span>

### <span data-ttu-id="316c6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="316c6-140">System.String</span></span>

## <span data-ttu-id="316c6-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="316c6-141">OUTPUTS</span></span>

## <span data-ttu-id="316c6-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="316c6-142">NOTES</span></span>

## <span data-ttu-id="316c6-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="316c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="316c6-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="316c6-145">Invoke-Azsqlela, Poolfailover</span><span class="sxs-lookup"><span data-stu-id="316c6-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="316c6-146">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="316c6-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="316c6-148">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="316c6-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="316c6-150">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="316c6-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="316c6-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="316c6-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
