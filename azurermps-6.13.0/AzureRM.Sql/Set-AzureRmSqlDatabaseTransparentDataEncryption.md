---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593624"
---
# <span data-ttu-id="83f90-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="83f90-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="83f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f90-102">SYNOPSIS</span></span>
<span data-ttu-id="83f90-103">Veritabanı için TDE özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="83f90-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83f90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83f90-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83f90-105">DESCRIPTION</span></span>
<span data-ttu-id="83f90-106">**Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet 'ı BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="83f90-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="83f90-107">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="83f90-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="83f90-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="83f90-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="83f90-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83f90-109">EXAMPLES</span></span>

### <span data-ttu-id="83f90-110">Örnek 1: veritabanı için TTE 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="83f90-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="83f90-111">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanı için ton 'ı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="83f90-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="83f90-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83f90-112">PARAMETERS</span></span>

### <span data-ttu-id="83f90-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83f90-113">-DatabaseName</span></span>
<span data-ttu-id="83f90-114">Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f90-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="83f90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f90-115">-DefaultProfile</span></span>
<span data-ttu-id="83f90-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="83f90-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83f90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f90-117">-ResourceGroupName</span></span>
<span data-ttu-id="83f90-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f90-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="83f90-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83f90-119">-ServerName</span></span>
<span data-ttu-id="83f90-120">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f90-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="83f90-121">Durumlu</span><span class="sxs-lookup"><span data-stu-id="83f90-121">-State</span></span>
<span data-ttu-id="83f90-122">TDE özelliğinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f90-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="83f90-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="83f90-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83f90-124">Etkin</span><span class="sxs-lookup"><span data-stu-id="83f90-124">Enabled</span></span> 
- <span data-ttu-id="83f90-125">DISABLED</span><span class="sxs-lookup"><span data-stu-id="83f90-125">Disabled</span></span>

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

### <span data-ttu-id="83f90-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="83f90-126">-Confirm</span></span>
<span data-ttu-id="83f90-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83f90-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f90-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f90-128">-WhatIf</span></span>
<span data-ttu-id="83f90-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83f90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f90-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83f90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f90-131">CommonParameters</span></span>
<span data-ttu-id="83f90-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83f90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f90-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f90-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83f90-134">INPUTS</span></span>

### <span data-ttu-id="83f90-135">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="83f90-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="83f90-136">System. String</span><span class="sxs-lookup"><span data-stu-id="83f90-136">System.String</span></span>

## <span data-ttu-id="83f90-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83f90-137">OUTPUTS</span></span>

### <span data-ttu-id="83f90-138">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="83f90-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="83f90-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83f90-139">NOTES</span></span>

## <span data-ttu-id="83f90-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83f90-140">RELATED LINKS</span></span>

[<span data-ttu-id="83f90-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="83f90-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="83f90-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="83f90-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="83f90-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="83f90-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


