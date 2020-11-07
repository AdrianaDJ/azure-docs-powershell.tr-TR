---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758956"
---
# <span data-ttu-id="3593e-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3593e-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="3593e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3593e-102">SYNOPSIS</span></span>
<span data-ttu-id="3593e-103">Sunucunun Gelişmiş tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3593e-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="3593e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3593e-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3593e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3593e-105">DESCRIPTION</span></span>
<span data-ttu-id="3593e-106">**Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet 'i, sunucunun Gelişmiş tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3593e-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="3593e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3593e-107">EXAMPLES</span></span>

### <span data-ttu-id="3593e-108">Örnek 1-Gelişmiş tehdit korumasını alır</span><span class="sxs-lookup"><span data-stu-id="3593e-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="3593e-109">Örnek 2-sunucu kaynağından Gelişmiş tehdit korumasını alır</span><span class="sxs-lookup"><span data-stu-id="3593e-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="3593e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3593e-110">PARAMETERS</span></span>

### <span data-ttu-id="3593e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3593e-111">-DefaultProfile</span></span>
<span data-ttu-id="3593e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3593e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3593e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3593e-113">-InputObject</span></span>
<span data-ttu-id="3593e-114">Gelişmiş tehdit koruması ilke işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="3593e-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="3593e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3593e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3593e-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3593e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="3593e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3593e-117">-ServerName</span></span>
<span data-ttu-id="3593e-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="3593e-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="3593e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3593e-119">CommonParameters</span></span>
<span data-ttu-id="3593e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3593e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3593e-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3593e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3593e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3593e-122">INPUTS</span></span>

### <span data-ttu-id="3593e-123">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="3593e-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="3593e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3593e-124">System.String</span></span>

## <span data-ttu-id="3593e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3593e-125">OUTPUTS</span></span>

### <span data-ttu-id="3593e-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3593e-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="3593e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3593e-127">NOTES</span></span>

## <span data-ttu-id="3593e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3593e-128">RELATED LINKS</span></span>
