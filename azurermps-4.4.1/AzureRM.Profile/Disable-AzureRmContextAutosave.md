---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 85c3791e9947ce6f7ad2ce365239da16cec17b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594206"
---
# <span data-ttu-id="257ca-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="257ca-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="257ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257ca-102">SYNOPSIS</span></span>
<span data-ttu-id="257ca-103">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="257ca-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="257ca-104">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="257ca-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257ca-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="257ca-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257ca-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="257ca-106">DESCRIPTION</span></span>
<span data-ttu-id="257ca-107">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="257ca-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="257ca-108">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="257ca-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="257ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="257ca-109">EXAMPLES</span></span>

### <span data-ttu-id="257ca-110">Bağlamı otomatik kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="257ca-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="257ca-111">Geçerli Kullanıcı için otomatik kaydetmeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="257ca-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="257ca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="257ca-112">PARAMETERS</span></span>

### <span data-ttu-id="257ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257ca-113">-DefaultProfile</span></span>
<span data-ttu-id="257ca-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="257ca-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257ca-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="257ca-115">-Scope</span></span>
<span data-ttu-id="257ca-116">Bağlam değişikliklerinin kapsamını belirler, örneğin, WHEA değişiklikleri yalnızca örnek işleme uygulanır veya bu kullanıcı tarafından başlatılan tüm oturumlar için</span><span class="sxs-lookup"><span data-stu-id="257ca-116">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="257ca-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="257ca-117">-Confirm</span></span>
<span data-ttu-id="257ca-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="257ca-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257ca-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257ca-119">-WhatIf</span></span>
<span data-ttu-id="257ca-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="257ca-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257ca-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="257ca-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257ca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257ca-122">CommonParameters</span></span>
<span data-ttu-id="257ca-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="257ca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257ca-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257ca-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257ca-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="257ca-125">INPUTS</span></span>

### <span data-ttu-id="257ca-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="257ca-126">None</span></span>

## <span data-ttu-id="257ca-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="257ca-127">OUTPUTS</span></span>

### <span data-ttu-id="257ca-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="257ca-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="257ca-129">Geçerli Kullanıcı için otomatik kaydetme özelliğinin etkinleştirilip etkinleştirilmediğini ve bağlam ve kimlik bilgileri dosyalarının kaydedildiği gibi geçerli otomatik kaydetme ayarları hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="257ca-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="257ca-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="257ca-130">NOTES</span></span>

## <span data-ttu-id="257ca-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="257ca-131">RELATED LINKS</span></span>

