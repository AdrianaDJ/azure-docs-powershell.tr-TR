---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 482a620552457993795ba03e2da9367df5efa614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937198"
---
# <span data-ttu-id="be7a6-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="be7a6-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="be7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="be7a6-103">Sunucuda gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="be7a6-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="be7a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be7a6-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be7a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="be7a6-106">**Disable-Azsqlserveradvancevseçdatasecurity** cmdlet 'ı sunucuda gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="be7a6-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="be7a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be7a6-107">EXAMPLES</span></span>

### <span data-ttu-id="be7a6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be7a6-108">Example 1</span></span>
### <span data-ttu-id="be7a6-109">Örnek 1-Gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="be7a6-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="be7a6-110">Örnek 2-sunucu kaynağından gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="be7a6-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="be7a6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be7a6-111">PARAMETERS</span></span>

### <span data-ttu-id="be7a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7a6-112">-DefaultProfile</span></span>
<span data-ttu-id="be7a6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be7a6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be7a6-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be7a6-114">-InputObject</span></span>
<span data-ttu-id="be7a6-115">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="be7a6-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be7a6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7a6-116">-ResourceGroupName</span></span>
<span data-ttu-id="be7a6-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be7a6-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="be7a6-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be7a6-118">-ServerName</span></span>
<span data-ttu-id="be7a6-119">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="be7a6-119">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be7a6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="be7a6-120">-Confirm</span></span>
<span data-ttu-id="be7a6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be7a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be7a6-122">-WhatIf</span></span>
<span data-ttu-id="be7a6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be7a6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be7a6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be7a6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7a6-125">CommonParameters</span></span>
<span data-ttu-id="be7a6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be7a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7a6-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be7a6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7a6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be7a6-128">INPUTS</span></span>

### <span data-ttu-id="be7a6-129">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="be7a6-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="be7a6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be7a6-130">System.String</span></span>

## <span data-ttu-id="be7a6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be7a6-131">OUTPUTS</span></span>

### <span data-ttu-id="be7a6-132">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="be7a6-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="be7a6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be7a6-133">NOTES</span></span>

## <span data-ttu-id="be7a6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be7a6-134">RELATED LINKS</span></span>
