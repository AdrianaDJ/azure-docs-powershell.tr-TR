---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589686"
---
# <span data-ttu-id="71166-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71166-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="71166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71166-102">SYNOPSIS</span></span>
<span data-ttu-id="71166-103">Yeni bir Active Directory kullanıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71166-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71166-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71166-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71166-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71166-105">DESCRIPTION</span></span>
<span data-ttu-id="71166-106">Yeni bir Active Directory kullanıcısı (iş/okul hesabı, ayrıca org-ID olarak da bilinir) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71166-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="71166-107">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="71166-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="71166-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71166-108">EXAMPLES</span></span>

### <span data-ttu-id="71166-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="71166-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="71166-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="71166-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="71166-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71166-111">PARAMETERS</span></span>

### <span data-ttu-id="71166-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71166-112">-DefaultProfile</span></span>
<span data-ttu-id="71166-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="71166-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71166-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71166-114">-DisplayName</span></span>
<span data-ttu-id="71166-115">Kullanıcının adres defterinde görüntülenecek ad.</span><span class="sxs-lookup"><span data-stu-id="71166-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="71166-116">örnek ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="71166-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71166-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="71166-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="71166-118">Kullanıcının sonraki başarılı oturum açmada parolasını değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="71166-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="71166-119">Sonraki başarılı oturum açmada parola değişimi için varsayılan davranış (false) olur.</span><span class="sxs-lookup"><span data-stu-id="71166-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71166-120">-Sanmutableıd</span><span class="sxs-lookup"><span data-stu-id="71166-120">-ImmutableId</span></span>
<span data-ttu-id="71166-121">Yalnızca kullanıcının Kullanıcı asıl adı (UPN) özelliği için federe bir etki alanı kullanıyorsanız belirtilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="71166-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71166-122">-Parola</span><span class="sxs-lookup"><span data-stu-id="71166-122">-Password</span></span>
<span data-ttu-id="71166-123">Kullanıcının parolası.</span><span class="sxs-lookup"><span data-stu-id="71166-123">Password for the user.</span></span>
<span data-ttu-id="71166-124">Kiracının parola karmaşıklığı gereksinimlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="71166-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="71166-125">Güçlü bir parola ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="71166-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71166-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="71166-126">-UserPrincipalName</span></span>
<span data-ttu-id="71166-127">Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="71166-127">The user principal name.</span></span>
<span data-ttu-id="71166-128">Örnek-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="71166-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71166-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="71166-129">-Confirm</span></span>
<span data-ttu-id="71166-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71166-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71166-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71166-131">-WhatIf</span></span>
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

### <span data-ttu-id="71166-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71166-132">CommonParameters</span></span>
<span data-ttu-id="71166-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71166-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71166-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71166-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71166-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71166-135">INPUTS</span></span>

### <span data-ttu-id="71166-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="71166-136">None</span></span>
<span data-ttu-id="71166-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="71166-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71166-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71166-138">OUTPUTS</span></span>

### <span data-ttu-id="71166-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="71166-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="71166-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71166-140">NOTES</span></span>

## <span data-ttu-id="71166-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71166-141">RELATED LINKS</span></span>

[<span data-ttu-id="71166-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71166-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="71166-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71166-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="71166-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71166-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
