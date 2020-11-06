---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: 0e875087d52ecddbf216c6e49db96fefdf63e82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593470"
---
# <span data-ttu-id="87078-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="87078-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="87078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87078-102">SYNOPSIS</span></span>
<span data-ttu-id="87078-103">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="87078-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87078-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87078-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87078-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87078-105">DESCRIPTION</span></span>
<span data-ttu-id="87078-106">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="87078-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="87078-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87078-107">EXAMPLES</span></span>

### <span data-ttu-id="87078-108">Geçerli Kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="87078-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="87078-109">Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma.</span><span class="sxs-lookup"><span data-stu-id="87078-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="87078-110">Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.</span><span class="sxs-lookup"><span data-stu-id="87078-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="87078-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87078-111">PARAMETERS</span></span>

### <span data-ttu-id="87078-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87078-112">-DefaultProfile</span></span>
<span data-ttu-id="87078-113">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="87078-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87078-114">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="87078-114">-Scope</span></span>
<span data-ttu-id="87078-115">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="87078-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="87078-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="87078-116">-Confirm</span></span>
<span data-ttu-id="87078-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87078-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87078-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87078-118">-WhatIf</span></span>
<span data-ttu-id="87078-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87078-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87078-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87078-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87078-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87078-121">CommonParameters</span></span>
<span data-ttu-id="87078-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87078-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87078-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87078-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87078-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87078-124">INPUTS</span></span>

### <span data-ttu-id="87078-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="87078-125">None</span></span>

## <span data-ttu-id="87078-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87078-126">OUTPUTS</span></span>

### <span data-ttu-id="87078-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="87078-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="87078-128">Geçerli Kullanıcı için otomatik kaydetme özelliğinin etkinleştirilip etkinleştirilmediğini ve bağlam ve kimlik bilgileri dosyalarının kaydedildiği gibi geçerli otomatik kaydetme ayarları hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="87078-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="87078-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87078-129">NOTES</span></span>

## <span data-ttu-id="87078-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87078-130">RELATED LINKS</span></span>

