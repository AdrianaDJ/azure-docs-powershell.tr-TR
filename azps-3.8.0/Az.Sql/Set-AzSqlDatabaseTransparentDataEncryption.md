---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098415"
---
# <span data-ttu-id="c87a7-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c87a7-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c87a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c87a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c87a7-103">Veritabanı için TDE özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="c87a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c87a7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c87a7-105">DESCRIPTION</span></span>
<span data-ttu-id="c87a7-106">**Set-AzSqlDatabaseTransparentDataEncryption** cmdlet 'ı BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="c87a7-107">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c87a7-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c87a7-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c87a7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c87a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c87a7-110">Örnek 1: veritabanı için TTE 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c87a7-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="c87a7-111">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanı için ton 'ı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c87a7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c87a7-112">PARAMETERS</span></span>

### <span data-ttu-id="c87a7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c87a7-113">-DatabaseName</span></span>
<span data-ttu-id="c87a7-114">Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c87a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87a7-115">-DefaultProfile</span></span>
<span data-ttu-id="c87a7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c87a7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c87a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c87a7-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c87a7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c87a7-119">-ServerName</span></span>
<span data-ttu-id="c87a7-120">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c87a7-121">Durumlu</span><span class="sxs-lookup"><span data-stu-id="c87a7-121">-State</span></span>
<span data-ttu-id="c87a7-122">TDE özelliğinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="c87a7-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c87a7-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c87a7-124">Etkin</span><span class="sxs-lookup"><span data-stu-id="c87a7-124">Enabled</span></span> 
- <span data-ttu-id="c87a7-125">DISABLED</span><span class="sxs-lookup"><span data-stu-id="c87a7-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87a7-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c87a7-126">-Confirm</span></span>
<span data-ttu-id="c87a7-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c87a7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87a7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87a7-128">-WhatIf</span></span>
<span data-ttu-id="c87a7-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c87a7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87a7-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c87a7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87a7-131">CommonParameters</span></span>
<span data-ttu-id="c87a7-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c87a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87a7-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c87a7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87a7-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c87a7-134">INPUTS</span></span>

### <span data-ttu-id="c87a7-135">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="c87a7-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="c87a7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c87a7-136">System.String</span></span>

## <span data-ttu-id="c87a7-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c87a7-137">OUTPUTS</span></span>

### <span data-ttu-id="c87a7-138">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c87a7-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c87a7-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c87a7-139">NOTES</span></span>

## <span data-ttu-id="c87a7-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c87a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="c87a7-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c87a7-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="c87a7-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c87a7-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c87a7-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c87a7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


