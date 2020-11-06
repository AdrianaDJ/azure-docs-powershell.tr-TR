---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592440"
---
# <span data-ttu-id="6c6dc-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="6c6dc-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="6c6dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6dc-103">Bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler, örneğin whterh içeriği otomatik olarak.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c6dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c6dc-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c6dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c6dc-105">DESCRIPTION</span></span>
<span data-ttu-id="6c6dc-106">İçeriğin otomatik olarak kaydedilip kaydedilmeyeceği ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde, bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="6c6dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c6dc-107">EXAMPLES</span></span>

### <span data-ttu-id="6c6dc-108">Geçerli oturumda bağlam kaydetme meta verilerini alma</span><span class="sxs-lookup"><span data-stu-id="6c6dc-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="6c6dc-109">İçeriğin kaydedilip kaydedilmeyeceğini öğrenmek isteyip istemediğinizi öğrenin.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="6c6dc-110">Yukarıdaki örnekte, otomatik kaydetme özelliği devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="6c6dc-111">Geçerli Kullanıcı için bağlam kaydetme meta verilerini alma</span><span class="sxs-lookup"><span data-stu-id="6c6dc-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="6c6dc-112">İçeriğin geçerli kullanıcı için varsayılan olarak kaydedilip kaydedilmeyeceğini öğrenmek isteyip istemediğinizi öğrenin.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="6c6dc-113">Bu, geçerli oturumda etkin olan ayarlardan farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="6c6dc-114">Yukarıdaki örnekte, Otomatik Kaydet özelliği etkinleştirilmiştir ve veriler varsayılan konuma kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="6c6dc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c6dc-115">PARAMETERS</span></span>

### <span data-ttu-id="6c6dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6dc-116">-DefaultProfile</span></span>
<span data-ttu-id="6c6dc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6c6dc-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c6dc-118">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6c6dc-118">-Scope</span></span>
<span data-ttu-id="6c6dc-119">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="6c6dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6dc-120">CommonParameters</span></span>
<span data-ttu-id="6c6dc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6dc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c6dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6dc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c6dc-123">INPUTS</span></span>

### <span data-ttu-id="6c6dc-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6c6dc-124">None</span></span>

## <span data-ttu-id="6c6dc-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c6dc-125">OUTPUTS</span></span>

### <span data-ttu-id="6c6dc-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="6c6dc-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="6c6dc-127">Geçerli Kullanıcı için otomatik kaydetme özelliğinin etkinleştirilip etkinleştirilmediğini ve bağlam ve kimlik bilgileri dosyalarının kaydedildiği gibi geçerli otomatik kaydetme ayarları hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="6c6dc-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="6c6dc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c6dc-128">NOTES</span></span>

## <span data-ttu-id="6c6dc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c6dc-129">RELATED LINKS</span></span>

