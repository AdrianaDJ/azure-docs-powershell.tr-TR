---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279437"
---
# <span data-ttu-id="ecf6e-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ecf6e-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ecf6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf6e-103">SQL Server için Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="ecf6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf6e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecf6e-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf6e-106">**Get-AzSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ecf6e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecf6e-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf6e-108">Örnek 1: sunucunun yöneticisi hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="ecf6e-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="ecf6e-109">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adındaki bir sunucuda Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ecf6e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecf6e-110">PARAMETERS</span></span>

### <span data-ttu-id="ecf6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf6e-111">-DefaultProfile</span></span>
<span data-ttu-id="ecf6e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ecf6e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecf6e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf6e-113">-ResourceGroupName</span></span>
<span data-ttu-id="ecf6e-114">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ecf6e-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecf6e-115">-ServerName</span></span>
<span data-ttu-id="ecf6e-116">Bu cmdlet 'in bilgi aldığı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ecf6e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ecf6e-117">-Confirm</span></span>
<span data-ttu-id="ecf6e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf6e-119">-WhatIf</span></span>
<span data-ttu-id="ecf6e-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf6e-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf6e-122">CommonParameters</span></span>
<span data-ttu-id="ecf6e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf6e-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf6e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-125">INPUTS</span></span>

### <span data-ttu-id="ecf6e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf6e-126">System.String</span></span>

## <span data-ttu-id="ecf6e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecf6e-127">OUTPUTS</span></span>

### <span data-ttu-id="ecf6e-128">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="ecf6e-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ecf6e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecf6e-129">NOTES</span></span>

## <span data-ttu-id="ecf6e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecf6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="ecf6e-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ecf6e-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ecf6e-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ecf6e-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ecf6e-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ecf6e-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ecf6e-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ecf6e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


