---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591879"
---
# <span data-ttu-id="cb0fc-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb0fc-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="cb0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0fc-103">Sunucunun Gelişmiş tehdit koruması ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb0fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb0fc-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0fc-106">**Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet 'i, sunucunun Gelişmiş tehdit koruması Ilkesini ele alıyor.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="cb0fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb0fc-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0fc-108">Örnek 1-Gelişmiş tehdit korumasını alır</span><span class="sxs-lookup"><span data-stu-id="cb0fc-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="cb0fc-109">Örnek 2-sunucu kaynağından Gelişmiş tehdit korumasını alır</span><span class="sxs-lookup"><span data-stu-id="cb0fc-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="cb0fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb0fc-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0fc-111">-DefaultProfile</span></span>
<span data-ttu-id="cb0fc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0fc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb0fc-113">-InputObject</span></span>
<span data-ttu-id="cb0fc-114">Gelişmiş tehdit koruması ilke işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="cb0fc-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="cb0fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb0fc-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb0fc-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb0fc-117">-ServerName</span></span>
<span data-ttu-id="cb0fc-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="cb0fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0fc-119">CommonParameters</span></span>
<span data-ttu-id="cb0fc-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb0fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0fc-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0fc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0fc-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb0fc-122">INPUTS</span></span>

### <span data-ttu-id="cb0fc-123">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="cb0fc-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="cb0fc-124">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb0fc-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cb0fc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cb0fc-125">System.String</span></span>

## <span data-ttu-id="cb0fc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb0fc-126">OUTPUTS</span></span>

### <span data-ttu-id="cb0fc-127">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb0fc-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="cb0fc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb0fc-128">NOTES</span></span>

## <span data-ttu-id="cb0fc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb0fc-129">RELATED LINKS</span></span>