---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f98e362c10a0773f16ae4b687e5d725fb12f5053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758957"
---
# <span data-ttu-id="22f67-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="22f67-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="22f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f67-102">SYNOPSIS</span></span>
<span data-ttu-id="22f67-103">SQL Server için Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="22f67-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="22f67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22f67-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22f67-105">DESCRIPTION</span></span>
<span data-ttu-id="22f67-106">**Get-AzSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="22f67-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="22f67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22f67-107">EXAMPLES</span></span>

### <span data-ttu-id="22f67-108">Örnek 1: sunucunun yöneticisi hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="22f67-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="22f67-109">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adındaki bir sunucuda Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="22f67-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="22f67-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22f67-110">PARAMETERS</span></span>

### <span data-ttu-id="22f67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f67-111">-DefaultProfile</span></span>
<span data-ttu-id="22f67-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="22f67-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22f67-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f67-113">-ResourceGroupName</span></span>
<span data-ttu-id="22f67-114">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22f67-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="22f67-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22f67-115">-ServerName</span></span>
<span data-ttu-id="22f67-116">Bu cmdlet 'in bilgi aldığı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22f67-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="22f67-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="22f67-117">-Confirm</span></span>
<span data-ttu-id="22f67-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22f67-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f67-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f67-119">-WhatIf</span></span>
<span data-ttu-id="22f67-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22f67-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f67-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22f67-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f67-122">CommonParameters</span></span>
<span data-ttu-id="22f67-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22f67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f67-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22f67-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f67-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22f67-125">INPUTS</span></span>

### <span data-ttu-id="22f67-126">System. String</span><span class="sxs-lookup"><span data-stu-id="22f67-126">System.String</span></span>

## <span data-ttu-id="22f67-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22f67-127">OUTPUTS</span></span>

### <span data-ttu-id="22f67-128">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="22f67-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="22f67-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22f67-129">NOTES</span></span>

## <span data-ttu-id="22f67-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22f67-130">RELATED LINKS</span></span>

[<span data-ttu-id="22f67-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="22f67-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="22f67-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="22f67-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="22f67-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="22f67-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


