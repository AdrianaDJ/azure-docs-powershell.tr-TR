---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762269"
---
# <span data-ttu-id="7fdec-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="7fdec-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="7fdec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fdec-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdec-103">Bir veritabanının GEÇERSIZ taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="7fdec-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fdec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fdec-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fdec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fdec-105">DESCRIPTION</span></span>
<span data-ttu-id="7fdec-106">**Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet 'i, BIR Azure SQL veritabanının saydam veri şifrelemesi (tde) taramasının ilerlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="7fdec-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="7fdec-107">Şifreleme yayılımı çalışmıyorsa, bu cmdlet boş bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fdec-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="7fdec-108">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7fdec-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="7fdec-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7fdec-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7fdec-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fdec-110">EXAMPLES</span></span>

### <span data-ttu-id="7fdec-111">Örnek 1: veritabanı için TTEKETKINLIK alma</span><span class="sxs-lookup"><span data-stu-id="7fdec-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="7fdec-112">Bu komut, server01 adındaki sunucudaki database01 adlı veritabanı için TDE etkinliği alır.</span><span class="sxs-lookup"><span data-stu-id="7fdec-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="7fdec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fdec-113">PARAMETERS</span></span>

### <span data-ttu-id="7fdec-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fdec-114">-DatabaseName</span></span>
<span data-ttu-id="7fdec-115">Bu cmdlet 'in TTEKŞIFRELEME etkinliği aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fdec-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="7fdec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdec-116">-ResourceGroupName</span></span>
<span data-ttu-id="7fdec-117">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fdec-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7fdec-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7fdec-118">-ServerName</span></span>
<span data-ttu-id="7fdec-119">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fdec-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7fdec-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fdec-120">-Confirm</span></span>
<span data-ttu-id="7fdec-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fdec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fdec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fdec-122">-WhatIf</span></span>
<span data-ttu-id="7fdec-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fdec-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fdec-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fdec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fdec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdec-125">-DefaultProfile</span></span>
<span data-ttu-id="7fdec-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fdec-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fdec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdec-127">CommonParameters</span></span>
<span data-ttu-id="7fdec-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fdec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdec-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fdec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdec-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fdec-130">INPUTS</span></span>

## <span data-ttu-id="7fdec-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fdec-131">OUTPUTS</span></span>

### <span data-ttu-id="7fdec-132">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="7fdec-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="7fdec-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fdec-133">NOTES</span></span>

## <span data-ttu-id="7fdec-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fdec-134">RELATED LINKS</span></span>

[<span data-ttu-id="7fdec-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7fdec-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="7fdec-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7fdec-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


