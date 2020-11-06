---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: d467ac4dd97e12fb72cbb81c523f7de43799ebbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592720"
---
# <span data-ttu-id="a97c5-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="a97c5-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="a97c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a97c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a97c5-103">Bir veritabanının GEÇERSIZ taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c5-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a97c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a97c5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a97c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a97c5-105">DESCRIPTION</span></span>
<span data-ttu-id="a97c5-106">**Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet 'i, BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c5-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="a97c5-107">Şifreleme yayılımı çalışmıyorsa, bu cmdlet boş bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="a97c5-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="a97c5-108">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="a97c5-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="a97c5-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a97c5-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a97c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a97c5-110">EXAMPLES</span></span>

### <span data-ttu-id="a97c5-111">Örnek 1: veritabanı için TTEKETKINLIK alma</span><span class="sxs-lookup"><span data-stu-id="a97c5-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="a97c5-112">Bu komut, server01 adındaki sunucudaki database01 adlı veritabanı için TDE etkinliği alır.</span><span class="sxs-lookup"><span data-stu-id="a97c5-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="a97c5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a97c5-113">PARAMETERS</span></span>

### <span data-ttu-id="a97c5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a97c5-114">-DatabaseName</span></span>
<span data-ttu-id="a97c5-115">Bu cmdlet 'in TTEKŞIFRELEME etkinliği aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a97c5-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="a97c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97c5-116">-DefaultProfile</span></span>
<span data-ttu-id="a97c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a97c5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a97c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="a97c5-119">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a97c5-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a97c5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a97c5-120">-ServerName</span></span>
<span data-ttu-id="a97c5-121">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a97c5-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a97c5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a97c5-122">-Confirm</span></span>
<span data-ttu-id="a97c5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a97c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a97c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a97c5-124">-WhatIf</span></span>
<span data-ttu-id="a97c5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a97c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a97c5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a97c5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a97c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97c5-127">CommonParameters</span></span>
<span data-ttu-id="a97c5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a97c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97c5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a97c5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97c5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a97c5-130">INPUTS</span></span>

### <span data-ttu-id="a97c5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a97c5-131">System.String</span></span>

## <span data-ttu-id="a97c5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a97c5-132">OUTPUTS</span></span>

### <span data-ttu-id="a97c5-133">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="a97c5-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="a97c5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a97c5-134">NOTES</span></span>

## <span data-ttu-id="a97c5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a97c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="a97c5-136">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a97c5-136">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="a97c5-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a97c5-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


