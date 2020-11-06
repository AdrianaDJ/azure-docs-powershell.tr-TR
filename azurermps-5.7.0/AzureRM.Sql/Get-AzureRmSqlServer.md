---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592885"
---
# <span data-ttu-id="dec1a-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="dec1a-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="dec1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dec1a-102">SYNOPSIS</span></span>
<span data-ttu-id="dec1a-103">SQL veritabanı sunucuları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="dec1a-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dec1a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dec1a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dec1a-105">DESCRIPTION</span></span>
<span data-ttu-id="dec1a-106">**Get-AzureRmSqlServer** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı sunucusu hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="dec1a-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="dec1a-107">Yalnızca bu sunucunun bilgilerini görmek için sunucunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dec1a-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="dec1a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dec1a-108">EXAMPLES</span></span>

### <span data-ttu-id="dec1a-109">Örnek 1: kaynak grubuna atanan tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="dec1a-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="dec1a-110">Bu komut, ResourceGroup01 kaynak grubuna atanmış tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dec1a-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="dec1a-111">Örnek 2: Azure SQL veritabanı sunucusu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="dec1a-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="dec1a-112">Bu komut, server01 adlı Azure SQL veritabanı sunucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dec1a-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="dec1a-113">Örnek 3: abonelikteki tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="dec1a-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="dec1a-114">Bu komut, geçerli abonelikteki tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dec1a-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="dec1a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dec1a-115">PARAMETERS</span></span>

### <span data-ttu-id="dec1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec1a-116">-DefaultProfile</span></span>
<span data-ttu-id="dec1a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dec1a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dec1a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec1a-118">-ResourceGroupName</span></span>
<span data-ttu-id="dec1a-119">Sunucuların atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec1a-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec1a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dec1a-120">-ServerName</span></span>
<span data-ttu-id="dec1a-121">Bu cmdlet 'in aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec1a-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec1a-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="dec1a-122">-Confirm</span></span>
<span data-ttu-id="dec1a-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dec1a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dec1a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dec1a-124">-WhatIf</span></span>
<span data-ttu-id="dec1a-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dec1a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dec1a-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dec1a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dec1a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec1a-127">CommonParameters</span></span>
<span data-ttu-id="dec1a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dec1a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec1a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec1a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec1a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dec1a-130">INPUTS</span></span>

### <span data-ttu-id="dec1a-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dec1a-131">None</span></span>
<span data-ttu-id="dec1a-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dec1a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dec1a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dec1a-133">OUTPUTS</span></span>

### <span data-ttu-id="dec1a-134">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="dec1a-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="dec1a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dec1a-135">NOTES</span></span>

## <span data-ttu-id="dec1a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dec1a-136">RELATED LINKS</span></span>

[<span data-ttu-id="dec1a-137">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="dec1a-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="dec1a-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="dec1a-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="dec1a-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="dec1a-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="dec1a-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="dec1a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


