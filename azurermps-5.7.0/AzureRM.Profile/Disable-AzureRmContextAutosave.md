---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573382"
---
# <span data-ttu-id="39d21-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="39d21-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="39d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d21-102">SYNOPSIS</span></span>
<span data-ttu-id="39d21-103">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="39d21-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="39d21-104">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="39d21-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39d21-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39d21-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39d21-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="39d21-106">DESCRIPTION</span></span>
<span data-ttu-id="39d21-107">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="39d21-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="39d21-108">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="39d21-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="39d21-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39d21-109">EXAMPLES</span></span>

### <span data-ttu-id="39d21-110">Bağlamı otomatik kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="39d21-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="39d21-111">Geçerli Kullanıcı için otomatik kaydetmeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="39d21-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="39d21-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39d21-112">PARAMETERS</span></span>

### <span data-ttu-id="39d21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d21-113">-DefaultProfile</span></span>
<span data-ttu-id="39d21-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="39d21-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d21-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="39d21-115">-Scope</span></span>
<span data-ttu-id="39d21-116">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="39d21-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d21-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="39d21-117">-Confirm</span></span>
<span data-ttu-id="39d21-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39d21-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d21-119">-WhatIf</span></span>
<span data-ttu-id="39d21-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39d21-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39d21-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39d21-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d21-122">CommonParameters</span></span>
<span data-ttu-id="39d21-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39d21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d21-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d21-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d21-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39d21-125">INPUTS</span></span>

### <span data-ttu-id="39d21-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="39d21-126">None</span></span>

## <span data-ttu-id="39d21-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39d21-127">OUTPUTS</span></span>

### <span data-ttu-id="39d21-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="39d21-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="39d21-129">Geçerli Kullanıcı için otomatik kaydetme özelliğinin etkinleştirilip etkinleştirilmediğini ve bağlam ve kimlik bilgileri dosyalarının kaydedildiği gibi geçerli otomatik kaydetme ayarları hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="39d21-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="39d21-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39d21-130">NOTES</span></span>

## <span data-ttu-id="39d21-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39d21-131">RELATED LINKS</span></span>

