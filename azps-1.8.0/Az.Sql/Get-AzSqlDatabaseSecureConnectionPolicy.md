---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: b29af2f5f8931876d1bf23d05072e92dc4eb588e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759016"
---
# <span data-ttu-id="497f4-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="497f4-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="497f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="497f4-102">SYNOPSIS</span></span>
<span data-ttu-id="497f4-103">Veritabanıyla ilgili güvenli bağlantı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="497f4-103">Gets the secure connection policy for a database.</span></span>

## <span data-ttu-id="497f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="497f4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="497f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="497f4-105">DESCRIPTION</span></span>
<span data-ttu-id="497f4-106">**Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet 'i, BIR Azure SQL veritabanının şifreli kanal ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="497f4-106">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="497f4-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="497f4-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="497f4-108">Bu cmdlet başarıyla çalıştıktan sonra, geçerli şifreli kanal ilkesini tanımlayan bir nesne ve ayrıca veritabanı tanımlayıcıları döndürür.</span><span class="sxs-lookup"><span data-stu-id="497f4-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="497f4-109">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="497f4-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="497f4-110">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="497f4-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="497f4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="497f4-111">EXAMPLES</span></span>

### <span data-ttu-id="497f4-112">Örnek 1: Azure SQL veritabanının şifreli kanal ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="497f4-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="497f4-113">Bu komut, database01 adındaki bir Azure SQL veritabanının şifreli kanal ilkesini server01.</span><span class="sxs-lookup"><span data-stu-id="497f4-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="497f4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="497f4-114">PARAMETERS</span></span>

### <span data-ttu-id="497f4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="497f4-115">-DatabaseName</span></span>
<span data-ttu-id="497f4-116">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="497f4-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="497f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497f4-117">-DefaultProfile</span></span>
<span data-ttu-id="497f4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="497f4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="497f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="497f4-120">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="497f4-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="497f4-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="497f4-121">-ServerName</span></span>
<span data-ttu-id="497f4-122">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="497f4-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="497f4-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="497f4-123">-Confirm</span></span>
<span data-ttu-id="497f4-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="497f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497f4-125">-WhatIf</span></span>
<span data-ttu-id="497f4-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="497f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497f4-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="497f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497f4-128">CommonParameters</span></span>
<span data-ttu-id="497f4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="497f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497f4-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="497f4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497f4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="497f4-131">INPUTS</span></span>

### <span data-ttu-id="497f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="497f4-132">System.String</span></span>

## <span data-ttu-id="497f4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="497f4-133">OUTPUTS</span></span>

### <span data-ttu-id="497f4-134">Microsoft. Azure. Commands. Sql. SecureConnection. model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="497f4-134">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="497f4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="497f4-135">NOTES</span></span>

## <span data-ttu-id="497f4-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="497f4-136">RELATED LINKS</span></span>
