---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590687"
---
# <span data-ttu-id="1978f-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="1978f-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="1978f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1978f-102">SYNOPSIS</span></span>
<span data-ttu-id="1978f-103">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="1978f-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1978f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1978f-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1978f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1978f-105">DESCRIPTION</span></span>
<span data-ttu-id="1978f-106">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="1978f-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="1978f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1978f-107">EXAMPLES</span></span>

### <span data-ttu-id="1978f-108">Geçerli Kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1978f-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="1978f-109">Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma.</span><span class="sxs-lookup"><span data-stu-id="1978f-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="1978f-110">Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.</span><span class="sxs-lookup"><span data-stu-id="1978f-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="1978f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1978f-111">PARAMETERS</span></span>

### <span data-ttu-id="1978f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1978f-112">-DefaultProfile</span></span>
<span data-ttu-id="1978f-113">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1978f-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1978f-114">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="1978f-114">-Scope</span></span>
<span data-ttu-id="1978f-115">Bağlam değişikliklerinin kapsamını belirler, örneğin, WHEA değişiklikleri yalnızca örnek işleme uygulanır veya bu kullanıcı tarafından başlatılan tüm oturumlar için</span><span class="sxs-lookup"><span data-stu-id="1978f-115">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="1978f-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="1978f-116">-Confirm</span></span>
<span data-ttu-id="1978f-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1978f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1978f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1978f-118">-WhatIf</span></span>
<span data-ttu-id="1978f-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1978f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1978f-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1978f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1978f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1978f-121">CommonParameters</span></span>
<span data-ttu-id="1978f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1978f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1978f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1978f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1978f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1978f-124">INPUTS</span></span>

### <span data-ttu-id="1978f-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1978f-125">None</span></span>

## <span data-ttu-id="1978f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1978f-126">OUTPUTS</span></span>

### <span data-ttu-id="1978f-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="1978f-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="1978f-128">Geçerli Kullanıcı için otomatik kaydetme özelliğinin etkinleştirilip etkinleştirilmediğini ve bağlam ve kimlik bilgileri dosyalarının kaydedildiği gibi geçerli otomatik kaydetme ayarları hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="1978f-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="1978f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1978f-129">NOTES</span></span>

## <span data-ttu-id="1978f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1978f-130">RELATED LINKS</span></span>

