---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: fb8769dcd8f989ad0715a799ce397eb0fe594126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933604"
---
# <span data-ttu-id="59cab-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59cab-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="59cab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59cab-102">SYNOPSIS</span></span>
<span data-ttu-id="59cab-103">SQL veritabanı sunucuları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="59cab-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="59cab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59cab-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59cab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59cab-105">DESCRIPTION</span></span>
<span data-ttu-id="59cab-106">**Get-AzSqlServer** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı sunucusu hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="59cab-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="59cab-107">Yalnızca bu sunucunun bilgilerini görmek için sunucunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="59cab-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="59cab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59cab-108">EXAMPLES</span></span>

### <span data-ttu-id="59cab-109">Örnek 1: kaynak grubuna atanan tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="59cab-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="59cab-110">Bu komut, ResourceGroup01 kaynak grubuna atanmış tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="59cab-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="59cab-111">Örnek 2: Azure SQL veritabanı sunucusu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="59cab-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="59cab-112">Bu komut, server01 adlı Azure SQL veritabanı sunucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="59cab-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="59cab-113">Örnek 3: abonelikteki tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="59cab-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
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

<span data-ttu-id="59cab-114">Bu komut, geçerli abonelikteki tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="59cab-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="59cab-115">Örnek 4: filtreleme kullanarak bir kaynak grubuna atanan tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="59cab-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
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

<span data-ttu-id="59cab-116">Bu komut, "Server" ile başlayan kaynak grubu ResourceGroup01 atanmış tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="59cab-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="59cab-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59cab-117">PARAMETERS</span></span>

### <span data-ttu-id="59cab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cab-118">-DefaultProfile</span></span>
<span data-ttu-id="59cab-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59cab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59cab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59cab-120">-ResourceGroupName</span></span>
<span data-ttu-id="59cab-121">Sunucuların atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59cab-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59cab-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59cab-122">-ServerName</span></span>
<span data-ttu-id="59cab-123">Bu cmdlet 'in aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59cab-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59cab-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="59cab-124">-Confirm</span></span>
<span data-ttu-id="59cab-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59cab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59cab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59cab-126">-WhatIf</span></span>
<span data-ttu-id="59cab-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59cab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59cab-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59cab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59cab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cab-129">CommonParameters</span></span>
<span data-ttu-id="59cab-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59cab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cab-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59cab-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cab-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59cab-132">INPUTS</span></span>

### <span data-ttu-id="59cab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="59cab-133">System.String</span></span>

## <span data-ttu-id="59cab-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59cab-134">OUTPUTS</span></span>

### <span data-ttu-id="59cab-135">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="59cab-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="59cab-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59cab-136">NOTES</span></span>

## <span data-ttu-id="59cab-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59cab-137">RELATED LINKS</span></span>

[<span data-ttu-id="59cab-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59cab-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="59cab-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59cab-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="59cab-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59cab-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="59cab-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="59cab-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


