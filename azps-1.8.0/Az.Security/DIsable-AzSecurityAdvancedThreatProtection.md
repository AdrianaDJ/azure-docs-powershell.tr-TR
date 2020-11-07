---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759265"
---
# <span data-ttu-id="fdcbe-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="fdcbe-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="fdcbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcbe-103">Depolama hesabı için Gelişmiş tehdit koruması ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="fdcbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdcbe-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcbe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcbe-106">`Disable-AzSecurityAdvancedThreatProtection`Cmdlet, bir depolama hesabı için tehdit protesto ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="fdcbe-107">Bu cmdlet 'i kullanmak için *RESOURCEID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="fdcbe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdcbe-108">EXAMPLES</span></span>

### <span data-ttu-id="fdcbe-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fdcbe-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="fdcbe-110">Bu komut, kaynak kimliği için Gelişmiş tehdit koruması ilkesini devre dışı bırakır `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="fdcbe-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="fdcbe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdcbe-111">PARAMETERS</span></span>

### <span data-ttu-id="fdcbe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcbe-112">-DefaultProfile</span></span>
<span data-ttu-id="fdcbe-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdcbe-114">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fdcbe-114">-ResourceId</span></span>
<span data-ttu-id="fdcbe-115">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fdcbe-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdcbe-116">-Confirm</span></span>
<span data-ttu-id="fdcbe-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcbe-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdcbe-118">-WhatIf</span></span>
<span data-ttu-id="fdcbe-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdcbe-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcbe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcbe-121">CommonParameters</span></span>
<span data-ttu-id="fdcbe-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdcbe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcbe-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdcbe-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcbe-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdcbe-124">INPUTS</span></span>

### <span data-ttu-id="fdcbe-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fdcbe-125">None</span></span>

## <span data-ttu-id="fdcbe-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdcbe-126">OUTPUTS</span></span>

### <span data-ttu-id="fdcbe-127">Microsoft. Azure. Commands. Security. modeller. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="fdcbe-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="fdcbe-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdcbe-128">NOTES</span></span>

## <span data-ttu-id="fdcbe-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdcbe-129">RELATED LINKS</span></span>
