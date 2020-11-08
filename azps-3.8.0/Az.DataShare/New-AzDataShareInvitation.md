---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: db4c1638d998db4f43210db4075353b108316e80
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097306"
---
# <span data-ttu-id="ec713-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="ec713-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="ec713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec713-102">SYNOPSIS</span></span>
<span data-ttu-id="ec713-103">Paylaşım için bir davet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec713-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="ec713-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec713-104">SYNTAX</span></span>

### <span data-ttu-id="ec713-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec713-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec713-106">Bydavetiemailparameterset</span><span class="sxs-lookup"><span data-stu-id="ec713-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec713-107">Bydavetitenantparameterset</span><span class="sxs-lookup"><span data-stu-id="ec713-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec713-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec713-108">DESCRIPTION</span></span>
<span data-ttu-id="ec713-109">**New-Azdatasharedavetiye** cmdlet 'i hedef tüketiciye sağlayıcı paylaşımı hakkında bilgi içeren bir davet gönderir.</span><span class="sxs-lookup"><span data-stu-id="ec713-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="ec713-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec713-110">EXAMPLES</span></span>

### <span data-ttu-id="ec713-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec713-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="ec713-112">Bu komut, Share AdsShare için bir davet adstest@micosoft.com</span><span class="sxs-lookup"><span data-stu-id="ec713-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@micosoft.com.</span></span>

## <span data-ttu-id="ec713-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec713-113">PARAMETERS</span></span>

### <span data-ttu-id="ec713-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec713-114">-AccountName</span></span>
<span data-ttu-id="ec713-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="ec713-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec713-116">-DefaultProfile</span></span>
<span data-ttu-id="ec713-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec713-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec713-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec713-118">-Name</span></span>
<span data-ttu-id="ec713-119">Azure veri paylaşımı davet adı</span><span class="sxs-lookup"><span data-stu-id="ec713-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec713-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec713-121">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ec713-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-122">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="ec713-122">-ShareName</span></span>
<span data-ttu-id="ec713-123">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="ec713-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="ec713-124">-TargetEmail</span></span>
<span data-ttu-id="ec713-125">Hedef e-posta kimliği</span><span class="sxs-lookup"><span data-stu-id="ec713-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="ec713-126">-TargetObjectId</span></span>
<span data-ttu-id="ec713-127">Hedef nesne kimliği</span><span class="sxs-lookup"><span data-stu-id="ec713-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-128">-Targettenantıd</span><span class="sxs-lookup"><span data-stu-id="ec713-128">-TargetTenantId</span></span>
<span data-ttu-id="ec713-129">Hedef Kiracı kimliği</span><span class="sxs-lookup"><span data-stu-id="ec713-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec713-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec713-130">-Confirm</span></span>
<span data-ttu-id="ec713-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec713-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec713-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec713-132">-WhatIf</span></span>
<span data-ttu-id="ec713-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec713-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec713-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec713-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec713-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec713-135">CommonParameters</span></span>
<span data-ttu-id="ec713-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec713-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec713-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec713-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec713-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec713-138">INPUTS</span></span>

### <span data-ttu-id="ec713-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ec713-139">None</span></span>

## <span data-ttu-id="ec713-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec713-140">OUTPUTS</span></span>

### <span data-ttu-id="ec713-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşıdavetiyesi</span><span class="sxs-lookup"><span data-stu-id="ec713-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="ec713-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec713-142">NOTES</span></span>

## <span data-ttu-id="ec713-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec713-143">RELATED LINKS</span></span>
