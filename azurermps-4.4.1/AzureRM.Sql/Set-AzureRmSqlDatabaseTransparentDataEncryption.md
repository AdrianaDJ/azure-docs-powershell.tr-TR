---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762394"
---
# <span data-ttu-id="32411-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="32411-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="32411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32411-102">SYNOPSIS</span></span>
<span data-ttu-id="32411-103">Veritabanı için TDE özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="32411-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32411-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32411-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32411-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32411-105">DESCRIPTION</span></span>
<span data-ttu-id="32411-106">**Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet 'ı BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="32411-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="32411-107">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="32411-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="32411-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="32411-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="32411-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32411-109">EXAMPLES</span></span>

### <span data-ttu-id="32411-110">Örnek 1: veritabanı için TTE 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="32411-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="32411-111">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanı için ton 'ı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="32411-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="32411-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32411-112">PARAMETERS</span></span>

### <span data-ttu-id="32411-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32411-113">-DatabaseName</span></span>
<span data-ttu-id="32411-114">Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32411-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="32411-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32411-115">-ResourceGroupName</span></span>
<span data-ttu-id="32411-116">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32411-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="32411-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32411-117">-ServerName</span></span>
<span data-ttu-id="32411-118">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32411-118">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="32411-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="32411-119">-State</span></span>
<span data-ttu-id="32411-120">TDE özelliğinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32411-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="32411-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="32411-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32411-122">Etkin</span><span class="sxs-lookup"><span data-stu-id="32411-122">Enabled</span></span> 
- <span data-ttu-id="32411-123">DISABLED</span><span class="sxs-lookup"><span data-stu-id="32411-123">Disabled</span></span>

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

### <span data-ttu-id="32411-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="32411-124">-Confirm</span></span>
<span data-ttu-id="32411-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32411-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32411-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32411-126">-WhatIf</span></span>
<span data-ttu-id="32411-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32411-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32411-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32411-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32411-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32411-129">-DefaultProfile</span></span>
<span data-ttu-id="32411-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32411-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32411-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32411-131">CommonParameters</span></span>
<span data-ttu-id="32411-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32411-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32411-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32411-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32411-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32411-134">INPUTS</span></span>

## <span data-ttu-id="32411-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32411-135">OUTPUTS</span></span>

### <span data-ttu-id="32411-136">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="32411-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="32411-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32411-137">NOTES</span></span>

## <span data-ttu-id="32411-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32411-138">RELATED LINKS</span></span>

[<span data-ttu-id="32411-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="32411-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="32411-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="32411-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="32411-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="32411-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


