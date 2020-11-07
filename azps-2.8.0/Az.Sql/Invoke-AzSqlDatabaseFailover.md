---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933855"
---
# <span data-ttu-id="02693-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="02693-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="02693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02693-102">SYNOPSIS</span></span>
<span data-ttu-id="02693-103">Bir veritabanını yerine ekleme.</span><span class="sxs-lookup"><span data-stu-id="02693-103">Failovers a database.</span></span>

## <span data-ttu-id="02693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02693-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02693-105">DESCRIPTION</span></span>
<span data-ttu-id="02693-106">Invoke-AzSqlDatabaseFailover cmdlet 'i Azure SQL veritabanı 'nı kullanın.</span><span class="sxs-lookup"><span data-stu-id="02693-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="02693-107">Veritabanı elastik bir havuzda ise bu komut, verilen veritabanı aynı elastik havuzda bulunan diğer veritabanlarını etkilemeden yük devretecektir.</span><span class="sxs-lookup"><span data-stu-id="02693-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="02693-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02693-108">EXAMPLES</span></span>

### <span data-ttu-id="02693-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02693-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="02693-110">Bu komut, "Server01" adlı sunucudaki "Database01" adlı veritabanını devreedecek</span><span class="sxs-lookup"><span data-stu-id="02693-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="02693-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02693-111">PARAMETERS</span></span>

### <span data-ttu-id="02693-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="02693-112">-AsJob</span></span>
<span data-ttu-id="02693-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02693-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02693-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02693-114">-DatabaseName</span></span>
<span data-ttu-id="02693-115">Yük devretmeye yönelik Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="02693-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="02693-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02693-116">-DefaultProfile</span></span>
<span data-ttu-id="02693-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02693-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02693-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02693-118">-Force</span></span>
<span data-ttu-id="02693-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="02693-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="02693-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02693-120">-PassThru</span></span>
<span data-ttu-id="02693-121">Başarılı bir yürütmede, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="02693-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="02693-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="02693-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02693-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02693-123">-ResourceGroupName</span></span>
<span data-ttu-id="02693-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="02693-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="02693-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02693-125">-ServerName</span></span>
<span data-ttu-id="02693-126">Veritabanının bulunduğu Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="02693-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="02693-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="02693-127">-Confirm</span></span>
<span data-ttu-id="02693-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02693-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02693-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02693-129">-WhatIf</span></span>
<span data-ttu-id="02693-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02693-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02693-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02693-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02693-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02693-132">CommonParameters</span></span>
<span data-ttu-id="02693-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02693-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02693-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02693-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02693-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02693-135">INPUTS</span></span>

### <span data-ttu-id="02693-136">System. String</span><span class="sxs-lookup"><span data-stu-id="02693-136">System.String</span></span>

## <span data-ttu-id="02693-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02693-137">OUTPUTS</span></span>

## <span data-ttu-id="02693-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02693-138">NOTES</span></span>

## <span data-ttu-id="02693-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02693-139">RELATED LINKS</span></span>

[<span data-ttu-id="02693-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="02693-141">Invoke-Azsqlela, Poolfailover</span><span class="sxs-lookup"><span data-stu-id="02693-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="02693-142">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="02693-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="02693-144">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="02693-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="02693-146">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02693-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="02693-147">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="02693-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
