---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 74956ff74beeb166a7788d0e577a86a4d2538ded
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933607"
---
# <span data-ttu-id="c9afc-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="c9afc-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="c9afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9afc-102">SYNOPSIS</span></span>
<span data-ttu-id="c9afc-103">Sunucunun gelişmiş veri güvenliği ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c9afc-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="c9afc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9afc-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9afc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9afc-105">DESCRIPTION</span></span>
<span data-ttu-id="c9afc-106">**Get-Azsqlserveradvancevseçdatasecuritpolicy** cmdlet 'i, sunucunun gelişmiş veri güvenliği ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c9afc-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="c9afc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9afc-107">EXAMPLES</span></span>

### <span data-ttu-id="c9afc-108">Örnek 1-sunucu gelişmiş veri güvenliğini alır</span><span class="sxs-lookup"><span data-stu-id="c9afc-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="c9afc-109">Örnek 2-sunucu kaynağından gelişmiş veri güvenliğini alır</span><span class="sxs-lookup"><span data-stu-id="c9afc-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="c9afc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9afc-110">PARAMETERS</span></span>

### <span data-ttu-id="c9afc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9afc-111">-DefaultProfile</span></span>
<span data-ttu-id="c9afc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9afc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9afc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9afc-113">-InputObject</span></span>
<span data-ttu-id="c9afc-114">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="c9afc-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9afc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9afc-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9afc-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9afc-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9afc-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9afc-117">-ServerName</span></span>
<span data-ttu-id="c9afc-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="c9afc-118">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9afc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9afc-119">CommonParameters</span></span>
<span data-ttu-id="c9afc-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9afc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c9afc-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9afc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9afc-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9afc-122">INPUTS</span></span>

### <span data-ttu-id="c9afc-123">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="c9afc-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="c9afc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c9afc-124">System.String</span></span>

## <span data-ttu-id="c9afc-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9afc-125">OUTPUTS</span></span>

### <span data-ttu-id="c9afc-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c9afc-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="c9afc-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9afc-127">NOTES</span></span>

## <span data-ttu-id="c9afc-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9afc-128">RELATED LINKS</span></span>