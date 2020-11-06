---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573302"
---
# <span data-ttu-id="b058d-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b058d-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="b058d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b058d-102">SYNOPSIS</span></span>
<span data-ttu-id="b058d-103">Var olan Active Directory kullanıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b058d-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b058d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b058d-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b058d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b058d-105">DESCRIPTION</span></span>
<span data-ttu-id="b058d-106">Var olan Active Directory kullanıcısını (iş/okul hesabı da, org-ID olarak da bilinir) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b058d-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="b058d-107">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="b058d-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="b058d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b058d-108">EXAMPLES</span></span>

### <span data-ttu-id="b058d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b058d-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b058d-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="b058d-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="b058d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b058d-111">PARAMETERS</span></span>

### <span data-ttu-id="b058d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b058d-112">-DefaultProfile</span></span>
<span data-ttu-id="b058d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b058d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b058d-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b058d-114">-DisplayName</span></span>
<span data-ttu-id="b058d-115">Kullanıcının adres defterinde görüntülenecek yeni ad.</span><span class="sxs-lookup"><span data-stu-id="b058d-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="b058d-116">Örnek-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="b058d-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="b058d-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="b058d-117">-EnableAccount</span></span>
<span data-ttu-id="b058d-118">Hesabı etkinleştirmek için doğru; Aksi takdirde, false.</span><span class="sxs-lookup"><span data-stu-id="b058d-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b058d-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="b058d-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="b058d-120">Yalnızca parolayı güncelleştirirken belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b058d-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="b058d-121">Aksi takdirde yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="b058d-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="b058d-122">Kullanıcının sonraki başarılı oturum açmada parolasını değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b058d-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="b058d-123">Sonraki başarılı oturum açmada parola değişimi için varsayılan davranış (false) olur.</span><span class="sxs-lookup"><span data-stu-id="b058d-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="b058d-124">-Parola</span><span class="sxs-lookup"><span data-stu-id="b058d-124">-Password</span></span>
<span data-ttu-id="b058d-125">Kullanıcı için yeni parola.</span><span class="sxs-lookup"><span data-stu-id="b058d-125">New password for the user.</span></span>
<span data-ttu-id="b058d-126">Kiracının parola karmaşıklığı gereksinimlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b058d-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="b058d-127">Güçlü bir parola ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="b058d-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b058d-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="b058d-128">-UPNOrObjectId</span></span>
<span data-ttu-id="b058d-129">Kullanıcı asıl adı (örneğin, ' someuser@contoso.com ') veya özelliklerin güncellenmesi gereken kullanıcının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="b058d-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="b058d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b058d-130">-Confirm</span></span>
<span data-ttu-id="b058d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b058d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b058d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b058d-132">-WhatIf</span></span>
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

### <span data-ttu-id="b058d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b058d-133">CommonParameters</span></span>
<span data-ttu-id="b058d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b058d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b058d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b058d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b058d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b058d-136">INPUTS</span></span>

### <span data-ttu-id="b058d-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b058d-137">None</span></span>
<span data-ttu-id="b058d-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b058d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b058d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b058d-139">OUTPUTS</span></span>

### <span data-ttu-id="b058d-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="b058d-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b058d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b058d-141">NOTES</span></span>

## <span data-ttu-id="b058d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b058d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b058d-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b058d-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="b058d-144">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b058d-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="b058d-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b058d-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

