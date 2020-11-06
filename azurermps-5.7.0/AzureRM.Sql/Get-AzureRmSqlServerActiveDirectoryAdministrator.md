---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588747"
---
# <span data-ttu-id="55d8a-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="55d8a-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="55d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="55d8a-103">SQL Server için Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="55d8a-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d8a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55d8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="55d8a-106">**Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="55d8a-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="55d8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="55d8a-108">Örnek 1: sunucunun yöneticisi hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="55d8a-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="55d8a-109">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adındaki bir sunucuda Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="55d8a-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="55d8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d8a-110">PARAMETERS</span></span>

### <span data-ttu-id="55d8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d8a-111">-DefaultProfile</span></span>
<span data-ttu-id="55d8a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="55d8a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55d8a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d8a-113">-ResourceGroupName</span></span>
<span data-ttu-id="55d8a-114">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d8a-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="55d8a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55d8a-115">-ServerName</span></span>
<span data-ttu-id="55d8a-116">Bu cmdlet 'in bilgi aldığı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d8a-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="55d8a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="55d8a-117">-Confirm</span></span>
<span data-ttu-id="55d8a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55d8a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d8a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d8a-119">-WhatIf</span></span>
<span data-ttu-id="55d8a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55d8a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55d8a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55d8a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d8a-122">CommonParameters</span></span>
<span data-ttu-id="55d8a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d8a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d8a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d8a-125">INPUTS</span></span>

### <span data-ttu-id="55d8a-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55d8a-126">None</span></span>
<span data-ttu-id="55d8a-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55d8a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55d8a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d8a-128">OUTPUTS</span></span>

### <span data-ttu-id="55d8a-129">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="55d8a-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="55d8a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d8a-130">NOTES</span></span>

## <span data-ttu-id="55d8a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d8a-131">RELATED LINKS</span></span>

[<span data-ttu-id="55d8a-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="55d8a-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="55d8a-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="55d8a-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="55d8a-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="55d8a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


