---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276291"
---
# <span data-ttu-id="b8926-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="b8926-101">Import-AzContext</span></span>

## <span data-ttu-id="b8926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8926-102">SYNOPSIS</span></span>
<span data-ttu-id="b8926-103">Azure kimlik doğrulama bilgilerini dosyadan yükler.</span><span class="sxs-lookup"><span data-stu-id="b8926-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="b8926-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8926-104">SYNTAX</span></span>

### <span data-ttu-id="b8926-105">ProfileFromDisk (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8926-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8926-106">Inmemoryprofile</span><span class="sxs-lookup"><span data-stu-id="b8926-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8926-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8926-107">DESCRIPTION</span></span>
<span data-ttu-id="b8926-108">Import-AzContext cmdlet, Azure ortamı ve bağlamını ayarlamak için bir dosyadan kimlik doğrulama bilgilerini yükler.</span><span class="sxs-lookup"><span data-stu-id="b8926-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="b8926-109">Geçerli oturumda çalıştırdığınız cmdlet 'ler, Azure Resource Manager 'daki isteklerin kimlik doğrulaması için bu bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="b8926-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="b8926-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8926-110">EXAMPLES</span></span>

### <span data-ttu-id="b8926-111">Örnek 1: AzureRmProfile bir bağlam Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b8926-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="b8926-112">Bu örnek, cmdlet 'e geçirilen PSAzureProfile 'daki bir bağlamı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="b8926-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="b8926-113">Örnek 2: JSON dosyasındaki bağlamı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b8926-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="b8926-114">Bu örnek, cmdlet 'e geçirilen JSON dosyasından bir bağlam seçer.</span><span class="sxs-lookup"><span data-stu-id="b8926-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="b8926-115">Bu JSON dosyası Save-AzContext 'den oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="b8926-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="b8926-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8926-116">PARAMETERS</span></span>

### <span data-ttu-id="b8926-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="b8926-117">-AzureContext</span></span>
<span data-ttu-id="b8926-118">{{Fill AzureContext açıklama}}</span><span class="sxs-lookup"><span data-stu-id="b8926-118">{{Fill AzureContext Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8926-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8926-119">-DefaultProfile</span></span>
<span data-ttu-id="b8926-120">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b8926-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8926-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="b8926-121">-Path</span></span>
<span data-ttu-id="b8926-122">Save-AzContext kullanılarak kaydedilen bağlam bilgilerinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8926-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8926-123">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="b8926-123">-Scope</span></span>
<span data-ttu-id="b8926-124">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="b8926-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b8926-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8926-125">-Confirm</span></span>
<span data-ttu-id="b8926-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8926-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8926-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8926-127">-WhatIf</span></span>
<span data-ttu-id="b8926-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8926-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8926-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8926-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8926-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8926-130">CommonParameters</span></span>
<span data-ttu-id="b8926-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8926-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8926-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8926-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8926-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8926-133">INPUTS</span></span>

### <span data-ttu-id="b8926-134">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="b8926-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="b8926-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b8926-135">System.String</span></span>

## <span data-ttu-id="b8926-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8926-136">OUTPUTS</span></span>

### <span data-ttu-id="b8926-137">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b8926-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="b8926-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8926-138">NOTES</span></span>

## <span data-ttu-id="b8926-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8926-139">RELATED LINKS</span></span>
