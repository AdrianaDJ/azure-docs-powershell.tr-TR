---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266819"
---
# <span data-ttu-id="a9e2c-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="a9e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e2c-103">Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="a9e2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9e2c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="a9e2c-106">**Remove-AzSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="a9e2c-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a9e2c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9e2c-108">EXAMPLES</span></span>

### <span data-ttu-id="a9e2c-109">Örnek 1: Azure SQL Server 'dan veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a9e2c-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a9e2c-110">Bu komut, Database01 adlı veritabanını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="a9e2c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9e2c-111">PARAMETERS</span></span>

### <span data-ttu-id="a9e2c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9e2c-112">-DatabaseName</span></span>
<span data-ttu-id="a9e2c-113">Bu cmdlet 'in kaldırdığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9e2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e2c-114">-DefaultProfile</span></span>
<span data-ttu-id="a9e2c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9e2c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e2c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a9e2c-116">-Force</span></span>
<span data-ttu-id="a9e2c-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9e2c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e2c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9e2c-119">Veritabanının atandığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a9e2c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9e2c-120">-ServerName</span></span>
<span data-ttu-id="a9e2c-121">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a9e2c-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9e2c-122">-Confirm</span></span>
<span data-ttu-id="a9e2c-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e2c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e2c-124">-WhatIf</span></span>
<span data-ttu-id="a9e2c-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e2c-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e2c-127">CommonParameters</span></span>
<span data-ttu-id="a9e2c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e2c-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a9e2c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e2c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9e2c-130">INPUTS</span></span>

### <span data-ttu-id="a9e2c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e2c-131">System.String</span></span>

## <span data-ttu-id="a9e2c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9e2c-132">OUTPUTS</span></span>

### <span data-ttu-id="a9e2c-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="a9e2c-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a9e2c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9e2c-134">NOTES</span></span>

## <span data-ttu-id="a9e2c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9e2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9e2c-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a9e2c-137">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="a9e2c-138">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="a9e2c-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="a9e2c-140">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9e2c-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="a9e2c-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a9e2c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


