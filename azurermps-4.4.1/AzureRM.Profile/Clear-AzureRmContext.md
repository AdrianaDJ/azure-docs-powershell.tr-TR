---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 5a640bf705040c3bb8ed0f7dc985693b2e57c873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764537"
---
# <span data-ttu-id="7bbbb-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="7bbbb-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="7bbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbbb-103">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bbbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bbbb-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bbbb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="7bbbb-106">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="7bbbb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bbbb-107">EXAMPLES</span></span>

### <span data-ttu-id="7bbbb-108">Global içeriği Temizle</span><span class="sxs-lookup"><span data-stu-id="7bbbb-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="7bbbb-109">Herhangi bir PowerShell oturumunun tüm hesap, abonelik ve kimlik bilgisi bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="7bbbb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bbbb-110">PARAMETERS</span></span>

### <span data-ttu-id="7bbbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbbb-111">-DefaultProfile</span></span>
<span data-ttu-id="7bbbb-112">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7bbbb-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bbbb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7bbbb-113">-Force</span></span>
<span data-ttu-id="7bbbb-114">Sormadan genel kapsamdan tüm kullanıcıları ve grupları silme</span><span class="sxs-lookup"><span data-stu-id="7bbbb-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbbb-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bbbb-115">-PassThru</span></span>
<span data-ttu-id="7bbbb-116">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="7bbbb-116">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbbb-117">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="7bbbb-117">-Scope</span></span>
<span data-ttu-id="7bbbb-118">Yalnızca geçerli PowerShell oturumunun veya tüm oturumların bağlamını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbbb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bbbb-119">-Confirm</span></span>
<span data-ttu-id="7bbbb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbbb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbbb-121">-WhatIf</span></span>
<span data-ttu-id="7bbbb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bbbb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbbb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbbb-124">CommonParameters</span></span>
<span data-ttu-id="7bbbb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbbb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bbbb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbbb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bbbb-127">INPUTS</span></span>

### <span data-ttu-id="7bbbb-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7bbbb-128">None</span></span>

## <span data-ttu-id="7bbbb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bbbb-129">OUTPUTS</span></span>

### <span data-ttu-id="7bbbb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7bbbb-130">System.Boolean</span></span>
<span data-ttu-id="7bbbb-131">Bağlam başarıyla temizlenmişse true, değilse false.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="7bbbb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bbbb-132">NOTES</span></span>

## <span data-ttu-id="7bbbb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bbbb-133">RELATED LINKS</span></span>

