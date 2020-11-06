---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 51e2c480b9a374136f2b040b8884cf85949b5fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591586"
---
# <span data-ttu-id="b7aad-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7aad-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="b7aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7aad-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aad-103">Veritabanıyla ilgili güvenli bağlantı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b7aad-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7aad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7aad-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7aad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7aad-105">DESCRIPTION</span></span>
<span data-ttu-id="b7aad-106">**Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet 'i, BIR Azure SQL veritabanının şifreli kanal ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b7aad-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="b7aad-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b7aad-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b7aad-108">Bu cmdlet başarıyla çalıştıktan sonra, geçerli şifreli kanal ilkesini tanımlayan bir nesne ve ayrıca veritabanı tanımlayıcıları döndürür.</span><span class="sxs-lookup"><span data-stu-id="b7aad-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="b7aad-109">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="b7aad-110">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b7aad-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7aad-111">EXAMPLES</span></span>

### <span data-ttu-id="b7aad-112">Örnek 1: Azure SQL veritabanının şifreli kanal ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="b7aad-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="b7aad-113">Bu komut, database01 adındaki bir Azure SQL veritabanının şifreli kanal ilkesini server01.</span><span class="sxs-lookup"><span data-stu-id="b7aad-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="b7aad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7aad-114">PARAMETERS</span></span>

### <span data-ttu-id="b7aad-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7aad-115">-DatabaseName</span></span>
<span data-ttu-id="b7aad-116">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-116">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aad-117">-DefaultProfile</span></span>
<span data-ttu-id="b7aad-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b7aad-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7aad-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7aad-120">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7aad-121">-ServerName</span></span>
<span data-ttu-id="b7aad-122">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-122">Specifies the name of server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7aad-123">-Confirm</span></span>
<span data-ttu-id="b7aad-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7aad-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7aad-125">-WhatIf</span></span>
<span data-ttu-id="b7aad-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7aad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7aad-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7aad-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7aad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aad-128">CommonParameters</span></span>
<span data-ttu-id="b7aad-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7aad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aad-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7aad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aad-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7aad-131">INPUTS</span></span>

### <span data-ttu-id="b7aad-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7aad-132">None</span></span>
<span data-ttu-id="b7aad-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b7aad-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7aad-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7aad-134">OUTPUTS</span></span>

### <span data-ttu-id="b7aad-135">Microsoft. Azure. Commands. Sql. Security. model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7aad-135">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="b7aad-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7aad-136">NOTES</span></span>

## <span data-ttu-id="b7aad-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7aad-137">RELATED LINKS</span></span>
