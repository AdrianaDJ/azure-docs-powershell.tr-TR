---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763344"
---
# <span data-ttu-id="1f452-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1f452-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="1f452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f452-102">SYNOPSIS</span></span>
<span data-ttu-id="1f452-103">Azure PowerShell cmdlet 'leriyle hedef için bir abonelik ve hesap seçin</span><span class="sxs-lookup"><span data-stu-id="1f452-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f452-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f452-104">SYNTAX</span></span>

### <span data-ttu-id="1f452-105">Giriş nesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f452-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f452-106">Bağlam adı</span><span class="sxs-lookup"><span data-stu-id="1f452-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="1f452-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f452-107">DESCRIPTION</span></span>
<span data-ttu-id="1f452-108">Azure PowerShell cmdlet 'leriyle hedef (veya bir hesap veya kiracı) aboneliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="1f452-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="1f452-109">Bu cmdlet 'in ardından, gelecekteki cmdlet 'ler seçilen içeriği hedefedecektir.</span><span class="sxs-lookup"><span data-stu-id="1f452-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="1f452-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f452-110">EXAMPLES</span></span>

### <span data-ttu-id="1f452-111">Örnek 1: adlandırılmış bir bağlamı hedefleyin</span><span class="sxs-lookup"><span data-stu-id="1f452-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="1f452-112">' Iş ' bağlamındaki hesap, kiracı ve abonelikteki gelecekteki Azure PowerShell cmdlet 'lerini hedefleyin.</span><span class="sxs-lookup"><span data-stu-id="1f452-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="1f452-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f452-113">PARAMETERS</span></span>

### <span data-ttu-id="1f452-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f452-114">-DefaultProfile</span></span>
<span data-ttu-id="1f452-115">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1f452-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f452-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f452-116">-InputObject</span></span>
<span data-ttu-id="1f452-117">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f452-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f452-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f452-118">-Name</span></span>
<span data-ttu-id="1f452-119">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="1f452-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f452-120">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="1f452-120">-Scope</span></span>
<span data-ttu-id="1f452-121">Bağlam değişikliklerinin kapsamını belirler, örneğin, WHEA değişiklikleri yalnızca örnek işleme uygulanır veya bu kullanıcı tarafından başlatılan tüm oturumlar için</span><span class="sxs-lookup"><span data-stu-id="1f452-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f452-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f452-122">-Confirm</span></span>
<span data-ttu-id="1f452-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f452-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f452-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f452-124">-WhatIf</span></span>
<span data-ttu-id="1f452-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f452-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f452-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f452-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f452-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f452-127">CommonParameters</span></span>
<span data-ttu-id="1f452-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f452-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f452-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f452-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f452-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f452-130">INPUTS</span></span>

### <span data-ttu-id="1f452-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f452-131">None</span></span>

## <span data-ttu-id="1f452-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f452-132">OUTPUTS</span></span>

### <span data-ttu-id="1f452-133">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="1f452-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="1f452-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f452-134">NOTES</span></span>

## <span data-ttu-id="1f452-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f452-135">RELATED LINKS</span></span>

