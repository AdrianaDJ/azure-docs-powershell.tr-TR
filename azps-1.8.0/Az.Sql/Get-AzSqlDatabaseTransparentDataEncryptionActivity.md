---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: bc072934fe8695cae0fd5f5762c1a31936997da9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759005"
---
# <span data-ttu-id="d7b75-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="d7b75-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="d7b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b75-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b75-103">Bir veritabanının GEÇERSIZ taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7b75-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="d7b75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7b75-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7b75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7b75-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b75-106">**Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet 'i, BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7b75-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="d7b75-107">Şifreleme yayılımı çalışmıyorsa, bu cmdlet boş bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7b75-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="d7b75-108">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="d7b75-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="d7b75-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d7b75-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d7b75-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7b75-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b75-111">Örnek 1: veritabanı için TTEKETKINLIK alma</span><span class="sxs-lookup"><span data-stu-id="d7b75-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="d7b75-112">Bu komut, server01 adındaki sunucudaki database01 adlı veritabanı için TDE etkinliği alır.</span><span class="sxs-lookup"><span data-stu-id="d7b75-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="d7b75-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7b75-113">PARAMETERS</span></span>

### <span data-ttu-id="d7b75-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7b75-114">-DatabaseName</span></span>
<span data-ttu-id="d7b75-115">Bu cmdlet 'in TTEKŞIFRELEME etkinliği aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b75-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="d7b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b75-116">-DefaultProfile</span></span>
<span data-ttu-id="d7b75-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d7b75-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7b75-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b75-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7b75-119">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b75-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d7b75-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7b75-120">-ServerName</span></span>
<span data-ttu-id="d7b75-121">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b75-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d7b75-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7b75-122">-Confirm</span></span>
<span data-ttu-id="d7b75-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7b75-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b75-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b75-124">-WhatIf</span></span>
<span data-ttu-id="d7b75-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7b75-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b75-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7b75-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b75-127">CommonParameters</span></span>
<span data-ttu-id="d7b75-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7b75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b75-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7b75-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b75-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7b75-130">INPUTS</span></span>

### <span data-ttu-id="d7b75-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b75-131">System.String</span></span>

## <span data-ttu-id="d7b75-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7b75-132">OUTPUTS</span></span>

### <span data-ttu-id="d7b75-133">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="d7b75-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="d7b75-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7b75-134">NOTES</span></span>

## <span data-ttu-id="d7b75-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7b75-135">RELATED LINKS</span></span>

[<span data-ttu-id="d7b75-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d7b75-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="d7b75-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d7b75-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


