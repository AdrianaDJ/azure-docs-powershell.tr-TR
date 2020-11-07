---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8d89b966da0fc9d5f0517c5faf777cb5d16efc33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758780"
---
# <span data-ttu-id="daa1a-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="daa1a-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="daa1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa1a-102">SYNOPSIS</span></span>
<span data-ttu-id="daa1a-103">Veritabanı için TDE özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="daa1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daa1a-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa1a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="daa1a-105">DESCRIPTION</span></span>
<span data-ttu-id="daa1a-106">**Set-AzSqlDatabaseTransparentDataEncryption** cmdlet 'ı BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="daa1a-107">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="daa1a-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="daa1a-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="daa1a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daa1a-109">EXAMPLES</span></span>

### <span data-ttu-id="daa1a-110">Örnek 1: veritabanı için TTE 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="daa1a-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="daa1a-111">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanı için ton 'ı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="daa1a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daa1a-112">PARAMETERS</span></span>

### <span data-ttu-id="daa1a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="daa1a-113">-DatabaseName</span></span>
<span data-ttu-id="daa1a-114">Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="daa1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa1a-115">-DefaultProfile</span></span>
<span data-ttu-id="daa1a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="daa1a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daa1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="daa1a-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="daa1a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="daa1a-119">-ServerName</span></span>
<span data-ttu-id="daa1a-120">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="daa1a-121">Durumlu</span><span class="sxs-lookup"><span data-stu-id="daa1a-121">-State</span></span>
<span data-ttu-id="daa1a-122">TDE özelliğinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="daa1a-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="daa1a-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="daa1a-124">Etkin</span><span class="sxs-lookup"><span data-stu-id="daa1a-124">Enabled</span></span> 
- <span data-ttu-id="daa1a-125">DISABLED</span><span class="sxs-lookup"><span data-stu-id="daa1a-125">Disabled</span></span>

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

### <span data-ttu-id="daa1a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="daa1a-126">-Confirm</span></span>
<span data-ttu-id="daa1a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="daa1a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa1a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa1a-128">-WhatIf</span></span>
<span data-ttu-id="daa1a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="daa1a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa1a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="daa1a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa1a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa1a-131">CommonParameters</span></span>
<span data-ttu-id="daa1a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daa1a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa1a-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="daa1a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa1a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daa1a-134">INPUTS</span></span>

### <span data-ttu-id="daa1a-135">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="daa1a-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="daa1a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="daa1a-136">System.String</span></span>

## <span data-ttu-id="daa1a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daa1a-137">OUTPUTS</span></span>

### <span data-ttu-id="daa1a-138">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="daa1a-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="daa1a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daa1a-139">NOTES</span></span>

## <span data-ttu-id="daa1a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daa1a-140">RELATED LINKS</span></span>

[<span data-ttu-id="daa1a-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="daa1a-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="daa1a-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="daa1a-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="daa1a-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="daa1a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


