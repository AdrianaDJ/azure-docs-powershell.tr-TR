---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319817"
---
# <span data-ttu-id="4eaa1-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="4eaa1-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="4eaa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="4eaa1-103">Sunucuda gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="4eaa1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4eaa1-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4eaa1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4eaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="4eaa1-106">**Disable-Azsqlserveradvancevseçdatasecurity** cmdlet 'ı sunucuda gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="4eaa1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4eaa1-107">EXAMPLES</span></span>

### <span data-ttu-id="4eaa1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4eaa1-108">Example 1</span></span>
### <span data-ttu-id="4eaa1-109">Örnek 2: sunucu gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4eaa1-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="4eaa1-110">Örnek 3: sunucu kaynağından gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4eaa1-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="4eaa1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4eaa1-111">PARAMETERS</span></span>

### <span data-ttu-id="4eaa1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eaa1-112">-DefaultProfile</span></span>
<span data-ttu-id="4eaa1-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eaa1-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eaa1-114">-InputObject</span></span>
<span data-ttu-id="4eaa1-115">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="4eaa1-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="4eaa1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eaa1-116">-ResourceGroupName</span></span>
<span data-ttu-id="4eaa1-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="4eaa1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eaa1-118">-ServerName</span></span>
<span data-ttu-id="4eaa1-119">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="4eaa1-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="4eaa1-120">-Confirm</span></span>
<span data-ttu-id="4eaa1-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eaa1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eaa1-122">-WhatIf</span></span>
<span data-ttu-id="4eaa1-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eaa1-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eaa1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eaa1-125">CommonParameters</span></span>
<span data-ttu-id="4eaa1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eaa1-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4eaa1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eaa1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4eaa1-128">INPUTS</span></span>

### <span data-ttu-id="4eaa1-129">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="4eaa1-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4eaa1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4eaa1-130">System.String</span></span>

## <span data-ttu-id="4eaa1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4eaa1-131">OUTPUTS</span></span>

### <span data-ttu-id="4eaa1-132">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4eaa1-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="4eaa1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4eaa1-133">NOTES</span></span>

## <span data-ttu-id="4eaa1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4eaa1-134">RELATED LINKS</span></span>
