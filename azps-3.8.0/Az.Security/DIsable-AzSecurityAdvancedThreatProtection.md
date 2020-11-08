---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 28e8521a283362989ff3ebace2f1e0a3e32c17a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098958"
---
# <span data-ttu-id="2e691-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2e691-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2e691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e691-102">SYNOPSIS</span></span>
<span data-ttu-id="2e691-103">Storage/cosmosDB hesabı için Gelişmiş tehdit koruması ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2e691-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2e691-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e691-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e691-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e691-105">DESCRIPTION</span></span>
<span data-ttu-id="2e691-106">`Disable-AzSecurityAdvancedThreatProtection`Cmdlet, bir depolama/cosmosDB hesabı için tehdit koruması ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2e691-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2e691-107">Bu cmdlet 'i kullanmak için *RESOURCEID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2e691-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2e691-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e691-108">EXAMPLES</span></span>

### <span data-ttu-id="2e691-109">Örnek 1: depolama hesabı</span><span class="sxs-lookup"><span data-stu-id="2e691-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2e691-110">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini devre dışı bırakır `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2e691-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2e691-111">Örnek 2: CosmosDB hesabı</span><span class="sxs-lookup"><span data-stu-id="2e691-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="2e691-112">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini devre dışı bırakır ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2e691-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="2e691-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e691-113">PARAMETERS</span></span>

### <span data-ttu-id="2e691-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e691-114">-DefaultProfile</span></span>
<span data-ttu-id="2e691-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e691-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e691-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2e691-116">-ResourceId</span></span>
<span data-ttu-id="2e691-117">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e691-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2e691-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e691-118">-Confirm</span></span>
<span data-ttu-id="2e691-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e691-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e691-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e691-120">-WhatIf</span></span>
<span data-ttu-id="2e691-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e691-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e691-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e691-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e691-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e691-123">CommonParameters</span></span>
<span data-ttu-id="2e691-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e691-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e691-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e691-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e691-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e691-126">INPUTS</span></span>

### <span data-ttu-id="2e691-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2e691-127">None</span></span>

## <span data-ttu-id="2e691-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e691-128">OUTPUTS</span></span>

### <span data-ttu-id="2e691-129">Microsoft. Azure. Commands. Security. modeller. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2e691-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2e691-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e691-130">NOTES</span></span>

## <span data-ttu-id="2e691-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e691-131">RELATED LINKS</span></span>
