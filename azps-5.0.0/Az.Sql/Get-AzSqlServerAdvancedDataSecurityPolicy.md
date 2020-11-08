---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279801"
---
# <span data-ttu-id="19d13-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="19d13-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="19d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d13-102">SYNOPSIS</span></span>
<span data-ttu-id="19d13-103">Sunucunun gelişmiş veri güvenliği ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="19d13-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="19d13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19d13-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19d13-105">DESCRIPTION</span></span>
<span data-ttu-id="19d13-106">**Get-Azsqlserveradvancevseçdatasecuritpolicy** cmdlet 'i, sunucunun gelişmiş veri güvenliği ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="19d13-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="19d13-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19d13-107">EXAMPLES</span></span>

### <span data-ttu-id="19d13-108">Örnek 1: sunucu gelişmiş veri güvenliğini alır</span><span class="sxs-lookup"><span data-stu-id="19d13-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="19d13-109">Örnek 2: sunucu kaynağından gelişmiş veri güvenliğini alır</span><span class="sxs-lookup"><span data-stu-id="19d13-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="19d13-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19d13-110">PARAMETERS</span></span>

### <span data-ttu-id="19d13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d13-111">-DefaultProfile</span></span>
<span data-ttu-id="19d13-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19d13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d13-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19d13-113">-InputObject</span></span>
<span data-ttu-id="19d13-114">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="19d13-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="19d13-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d13-115">-ResourceGroupName</span></span>
<span data-ttu-id="19d13-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="19d13-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="19d13-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19d13-117">-ServerName</span></span>
<span data-ttu-id="19d13-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="19d13-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="19d13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d13-119">CommonParameters</span></span>
<span data-ttu-id="19d13-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19d13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d13-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19d13-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d13-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19d13-122">INPUTS</span></span>

### <span data-ttu-id="19d13-123">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="19d13-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="19d13-124">System. String</span><span class="sxs-lookup"><span data-stu-id="19d13-124">System.String</span></span>

## <span data-ttu-id="19d13-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19d13-125">OUTPUTS</span></span>

### <span data-ttu-id="19d13-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="19d13-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="19d13-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19d13-127">NOTES</span></span>

## <span data-ttu-id="19d13-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19d13-128">RELATED LINKS</span></span>
