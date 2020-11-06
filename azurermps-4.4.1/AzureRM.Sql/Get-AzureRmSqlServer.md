---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592995"
---
# <span data-ttu-id="3fcc0-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fcc0-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="3fcc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcc0-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcc0-103">SQL veritabanı sunucuları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fcc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fcc0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fcc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fcc0-105">DESCRIPTION</span></span>
<span data-ttu-id="3fcc0-106">**Get-AzureRmSqlServer** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı sunucusu hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="3fcc0-107">Yalnızca bu sunucunun bilgilerini görmek için sunucunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="3fcc0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fcc0-108">EXAMPLES</span></span>

### <span data-ttu-id="3fcc0-109">Örnek 1: kaynak grubuna atanan tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="3fcc0-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="3fcc0-110">Bu komut, ResourceGroup01 kaynak grubuna atanmış tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="3fcc0-111">Örnek 2: Azure SQL veritabanı sunucusu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="3fcc0-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="3fcc0-112">Bu komut, server01 adlı Azure SQL veritabanı sunucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="3fcc0-113">Örnek 3: abonelikteki tüm SQL Server örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="3fcc0-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="3fcc0-114">Bu komut, geçerli abonelikteki tüm Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="3fcc0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fcc0-115">PARAMETERS</span></span>

### <span data-ttu-id="3fcc0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcc0-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fcc0-117">Sunucuların atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-117">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcc0-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fcc0-118">-ServerName</span></span>
<span data-ttu-id="3fcc0-119">Bu cmdlet 'in aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-119">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcc0-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="3fcc0-120">-Confirm</span></span>
<span data-ttu-id="3fcc0-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcc0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcc0-122">-WhatIf</span></span>
<span data-ttu-id="3fcc0-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fcc0-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcc0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcc0-125">-DefaultProfile</span></span>
<span data-ttu-id="3fcc0-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fcc0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcc0-127">CommonParameters</span></span>
<span data-ttu-id="3fcc0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fcc0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcc0-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fcc0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcc0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fcc0-130">INPUTS</span></span>

## <span data-ttu-id="3fcc0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fcc0-131">OUTPUTS</span></span>

### <span data-ttu-id="3fcc0-132">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="3fcc0-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3fcc0-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fcc0-133">NOTES</span></span>

## <span data-ttu-id="3fcc0-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fcc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="3fcc0-135">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fcc0-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="3fcc0-136">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fcc0-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="3fcc0-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fcc0-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="3fcc0-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="3fcc0-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


