---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759057"
---
# <span data-ttu-id="4431a-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4431a-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="4431a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4431a-102">SYNOPSIS</span></span>
<span data-ttu-id="4431a-103">Sunucuda Gelişmiş tehdit korumasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4431a-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="4431a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4431a-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4431a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4431a-105">DESCRIPTION</span></span>
<span data-ttu-id="4431a-106">**Enable-AzSqlServerAdvancedThreatProtection** cmdlet 'ı sunucuda Gelişmiş tehdit korumasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4431a-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="4431a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4431a-107">EXAMPLES</span></span>

### <span data-ttu-id="4431a-108">Örnek 1-sunucu Gelişmiş tehdit korumasını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4431a-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="4431a-109">Örnek 2-sunucu kaynağından Gelişmiş tehdit korumasını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4431a-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="4431a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4431a-110">PARAMETERS</span></span>

### <span data-ttu-id="4431a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4431a-111">-DefaultProfile</span></span>
<span data-ttu-id="4431a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4431a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4431a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4431a-113">-InputObject</span></span>
<span data-ttu-id="4431a-114">Gelişmiş tehdit koruması ilke işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="4431a-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="4431a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4431a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4431a-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4431a-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="4431a-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4431a-117">-ServerName</span></span>
<span data-ttu-id="4431a-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="4431a-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="4431a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4431a-119">-Confirm</span></span>
<span data-ttu-id="4431a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4431a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4431a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4431a-121">-WhatIf</span></span>
<span data-ttu-id="4431a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4431a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4431a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4431a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4431a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4431a-124">CommonParameters</span></span>
<span data-ttu-id="4431a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4431a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4431a-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4431a-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4431a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4431a-127">INPUTS</span></span>

### <span data-ttu-id="4431a-128">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="4431a-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4431a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4431a-129">System.String</span></span>

## <span data-ttu-id="4431a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4431a-130">OUTPUTS</span></span>

### <span data-ttu-id="4431a-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4431a-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="4431a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4431a-132">NOTES</span></span>

## <span data-ttu-id="4431a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4431a-133">RELATED LINKS</span></span>
