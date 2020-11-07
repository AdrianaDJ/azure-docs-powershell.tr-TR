---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 118a81287000bd4d3fc3f20881814e14de4c42c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753737"
---
# <span data-ttu-id="2df12-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="2df12-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="2df12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2df12-102">SYNOPSIS</span></span>
<span data-ttu-id="2df12-103">İçeriğin otomatik olarak kaydedilip kaydedilmeyeceği ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde, bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2df12-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="2df12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2df12-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2df12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2df12-105">DESCRIPTION</span></span>
<span data-ttu-id="2df12-106">İçeriğin otomatik olarak kaydedilip kaydedilmeyeceği ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde, bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2df12-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="2df12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2df12-107">EXAMPLES</span></span>

### <span data-ttu-id="2df12-108">Geçerli oturumda bağlam kaydetme meta verilerini alma</span><span class="sxs-lookup"><span data-stu-id="2df12-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="2df12-109">İçeriğin kaydedilip kaydedilmeyeceği hakkında ayrıntılı bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="2df12-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="2df12-110">Yukarıdaki örnekte, otomatik kaydetme özelliği devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="2df12-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="2df12-111">Geçerli Kullanıcı için bağlam kaydetme meta verilerini alma</span><span class="sxs-lookup"><span data-stu-id="2df12-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="2df12-112">İçeriğin geçerli kullanıcı için varsayılan olarak kaydedilip kaydedilmeyeceği hakkında ayrıntılı bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="2df12-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="2df12-113">Bu, geçerli oturumda etkin olan ayarlardan farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="2df12-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="2df12-114">Yukarıdaki örnekte, Otomatik Kaydet özelliği etkinleştirilmiştir ve veriler varsayılan konuma kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2df12-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="2df12-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2df12-115">PARAMETERS</span></span>

### <span data-ttu-id="2df12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df12-116">-DefaultProfile</span></span>
<span data-ttu-id="2df12-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2df12-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2df12-118">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="2df12-118">-Scope</span></span>
<span data-ttu-id="2df12-119">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="2df12-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2df12-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df12-120">CommonParameters</span></span>
<span data-ttu-id="2df12-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2df12-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df12-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df12-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df12-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2df12-123">INPUTS</span></span>

### <span data-ttu-id="2df12-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2df12-124">None</span></span>

## <span data-ttu-id="2df12-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2df12-125">OUTPUTS</span></span>

### <span data-ttu-id="2df12-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="2df12-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="2df12-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2df12-127">NOTES</span></span>

## <span data-ttu-id="2df12-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2df12-128">RELATED LINKS</span></span>
