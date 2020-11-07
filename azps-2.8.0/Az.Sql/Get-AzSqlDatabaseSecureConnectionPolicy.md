---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933657"
---
# <span data-ttu-id="a978b-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a978b-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="a978b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a978b-102">SYNOPSIS</span></span>
<span data-ttu-id="a978b-103">Veritabanıyla ilgili güvenli bağlantı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a978b-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="a978b-104">Güvenli bağlantı kullanım dışıdır ve bu komut sonraki sürümde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a978b-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="a978b-105">Bağlantı dizelerini görüntülemek için lütfen Azure portalında SQL veritabanı Blade 'i kullanın</span><span class="sxs-lookup"><span data-stu-id="a978b-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="a978b-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a978b-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a978b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a978b-107">DESCRIPTION</span></span>
<span data-ttu-id="a978b-108">**Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet 'i, BIR Azure SQL veritabanının şifreli kanal ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a978b-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="a978b-109">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a978b-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a978b-110">Bu cmdlet başarıyla çalıştıktan sonra, geçerli şifreli kanal ilkesini tanımlayan bir nesne ve ayrıca veritabanı tanımlayıcıları döndürür.</span><span class="sxs-lookup"><span data-stu-id="a978b-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="a978b-111">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="a978b-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="a978b-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a978b-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a978b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a978b-113">EXAMPLES</span></span>

### <span data-ttu-id="a978b-114">Örnek 1: Azure SQL veritabanının şifreli kanal ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="a978b-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
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

<span data-ttu-id="a978b-115">Bu komut, database01 adındaki bir Azure SQL veritabanının şifreli kanal ilkesini server01.</span><span class="sxs-lookup"><span data-stu-id="a978b-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="a978b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a978b-116">PARAMETERS</span></span>

### <span data-ttu-id="a978b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a978b-117">-DatabaseName</span></span>
<span data-ttu-id="a978b-118">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a978b-118">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a978b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a978b-119">-DefaultProfile</span></span>
<span data-ttu-id="a978b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a978b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a978b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a978b-121">-ResourceGroupName</span></span>
<span data-ttu-id="a978b-122">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a978b-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a978b-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a978b-123">-ServerName</span></span>
<span data-ttu-id="a978b-124">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a978b-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="a978b-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a978b-125">-Confirm</span></span>
<span data-ttu-id="a978b-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a978b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a978b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a978b-127">-WhatIf</span></span>
<span data-ttu-id="a978b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a978b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a978b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a978b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a978b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a978b-130">CommonParameters</span></span>
<span data-ttu-id="a978b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a978b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a978b-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a978b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a978b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a978b-133">INPUTS</span></span>

### <span data-ttu-id="a978b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a978b-134">System.String</span></span>

## <span data-ttu-id="a978b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a978b-135">OUTPUTS</span></span>

### <span data-ttu-id="a978b-136">Microsoft. Azure. Commands. Sql. SecureConnection. model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a978b-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="a978b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a978b-137">NOTES</span></span>

## <span data-ttu-id="a978b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a978b-138">RELATED LINKS</span></span>
