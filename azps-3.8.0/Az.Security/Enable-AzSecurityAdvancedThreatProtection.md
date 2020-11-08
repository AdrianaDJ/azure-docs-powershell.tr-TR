---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 7e1bf5552d8c6fd6c7dff0c4478557059b0bc78a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097328"
---
# <span data-ttu-id="a9390-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9390-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9390-102">SYNOPSIS</span></span>
<span data-ttu-id="a9390-103">Storage/cosmosDB hesabı için Gelişmiş tehdit koruması ilkesini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a9390-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="a9390-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9390-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9390-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9390-105">DESCRIPTION</span></span>
<span data-ttu-id="a9390-106">`Enable-AzSecurityAdvancedThreatProtection`Cmdlet, bir depolama/cosmosDB hesabı için tehdit koruması ilkesini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a9390-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="a9390-107">Bu cmdlet 'i kullanmak için *RESOURCEID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a9390-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="a9390-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9390-108">EXAMPLES</span></span>

### <span data-ttu-id="a9390-109">Örnek 1: depolama hesabı</span><span class="sxs-lookup"><span data-stu-id="a9390-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="a9390-110">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini etkinleştirmiştir `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="a9390-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="a9390-111">Örnek 2: CosmosDB hesabı</span><span class="sxs-lookup"><span data-stu-id="a9390-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="a9390-112">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini etkinleştirmiştir ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="a9390-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="a9390-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9390-113">PARAMETERS</span></span>

### <span data-ttu-id="a9390-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9390-114">-DefaultProfile</span></span>
<span data-ttu-id="a9390-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9390-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9390-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a9390-116">-ResourceId</span></span>
<span data-ttu-id="a9390-117">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a9390-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a9390-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9390-118">-Confirm</span></span>
<span data-ttu-id="a9390-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9390-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9390-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9390-120">-WhatIf</span></span>
<span data-ttu-id="a9390-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9390-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9390-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9390-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9390-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9390-123">CommonParameters</span></span>
<span data-ttu-id="a9390-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9390-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9390-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9390-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9390-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9390-126">INPUTS</span></span>

### <span data-ttu-id="a9390-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9390-127">None</span></span>

## <span data-ttu-id="a9390-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9390-128">OUTPUTS</span></span>

### <span data-ttu-id="a9390-129">Microsoft. Azure. Commands. Security. modeller. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9390-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9390-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9390-130">NOTES</span></span>

## <span data-ttu-id="a9390-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9390-131">RELATED LINKS</span></span>
