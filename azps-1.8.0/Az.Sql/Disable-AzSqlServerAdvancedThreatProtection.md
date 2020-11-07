---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759059"
---
# <span data-ttu-id="69883-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="69883-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="69883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69883-102">SYNOPSIS</span></span>
<span data-ttu-id="69883-103">Sunucuda Gelişmiş tehdit korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="69883-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="69883-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69883-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69883-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69883-105">DESCRIPTION</span></span>
<span data-ttu-id="69883-106">**Disable-AzSqlServerAdvancedThreatProtection** cmdlet 'ı sunucuda Gelişmiş tehdit korumasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="69883-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="69883-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69883-107">EXAMPLES</span></span>

### <span data-ttu-id="69883-108">Örnek 1-Gelişmiş tehdit korumasını devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="69883-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="69883-109">Örnek 2-sunucu kaynağından Gelişmiş tehdit korumasını devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="69883-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="69883-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69883-110">PARAMETERS</span></span>

### <span data-ttu-id="69883-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69883-111">-DefaultProfile</span></span>
<span data-ttu-id="69883-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69883-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69883-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69883-113">-InputObject</span></span>
<span data-ttu-id="69883-114">Gelişmiş tehdit koruması ilke işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="69883-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="69883-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69883-115">-ResourceGroupName</span></span>
<span data-ttu-id="69883-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69883-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="69883-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69883-117">-ServerName</span></span>
<span data-ttu-id="69883-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="69883-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="69883-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="69883-119">-Confirm</span></span>
<span data-ttu-id="69883-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69883-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69883-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69883-121">-WhatIf</span></span>
<span data-ttu-id="69883-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69883-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69883-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69883-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69883-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69883-124">CommonParameters</span></span>
<span data-ttu-id="69883-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69883-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69883-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69883-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69883-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69883-127">INPUTS</span></span>

### <span data-ttu-id="69883-128">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="69883-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="69883-129">System. String</span><span class="sxs-lookup"><span data-stu-id="69883-129">System.String</span></span>

## <span data-ttu-id="69883-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69883-130">OUTPUTS</span></span>

### <span data-ttu-id="69883-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="69883-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="69883-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69883-132">NOTES</span></span>

## <span data-ttu-id="69883-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69883-133">RELATED LINKS</span></span>
