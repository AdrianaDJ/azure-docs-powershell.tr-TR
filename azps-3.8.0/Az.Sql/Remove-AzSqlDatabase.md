---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937622"
---
# <span data-ttu-id="643e3-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="643e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="643e3-102">SYNOPSIS</span></span>
<span data-ttu-id="643e3-103">Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="643e3-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="643e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="643e3-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="643e3-105">DESCRIPTION</span></span>
<span data-ttu-id="643e3-106">**Remove-AzSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="643e3-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="643e3-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="643e3-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="643e3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="643e3-108">EXAMPLES</span></span>

### <span data-ttu-id="643e3-109">Örnek 1: Azure SQL Server 'dan veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="643e3-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="643e3-110">Bu komut, Database01 adlı veritabanını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="643e3-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="643e3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="643e3-111">PARAMETERS</span></span>

### <span data-ttu-id="643e3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="643e3-112">-DatabaseName</span></span>
<span data-ttu-id="643e3-113">Bu cmdlet 'in kaldırdığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="643e3-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="643e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643e3-114">-DefaultProfile</span></span>
<span data-ttu-id="643e3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="643e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="643e3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="643e3-116">-Force</span></span>
<span data-ttu-id="643e3-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="643e3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="643e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="643e3-119">Veritabanının atandığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="643e3-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="643e3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="643e3-120">-ServerName</span></span>
<span data-ttu-id="643e3-121">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="643e3-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="643e3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="643e3-122">-Confirm</span></span>
<span data-ttu-id="643e3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="643e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643e3-124">-WhatIf</span></span>
<span data-ttu-id="643e3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="643e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643e3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="643e3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643e3-127">CommonParameters</span></span>
<span data-ttu-id="643e3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="643e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643e3-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="643e3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643e3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="643e3-130">INPUTS</span></span>

### <span data-ttu-id="643e3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="643e3-131">System.String</span></span>

## <span data-ttu-id="643e3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="643e3-132">OUTPUTS</span></span>

### <span data-ttu-id="643e3-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="643e3-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="643e3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="643e3-134">NOTES</span></span>

## <span data-ttu-id="643e3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="643e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="643e3-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="643e3-137">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="643e3-138">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="643e3-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="643e3-140">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="643e3-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="643e3-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="643e3-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


