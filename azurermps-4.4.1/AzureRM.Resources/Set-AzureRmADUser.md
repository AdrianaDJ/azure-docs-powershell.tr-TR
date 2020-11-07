---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762195"
---
# <span data-ttu-id="84c15-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="84c15-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="84c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84c15-102">SYNOPSIS</span></span>
<span data-ttu-id="84c15-103">Var olan Active Directory kullanıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84c15-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84c15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84c15-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84c15-105">DESCRIPTION</span></span>
<span data-ttu-id="84c15-106">Var olan Active Directory kullanıcısını (iş/okul hesabı da, org-ID olarak da bilinir) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84c15-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="84c15-107">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="84c15-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="84c15-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84c15-108">EXAMPLES</span></span>

### <span data-ttu-id="84c15-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84c15-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="84c15-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="84c15-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="84c15-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84c15-111">PARAMETERS</span></span>

### <span data-ttu-id="84c15-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="84c15-112">-DisplayName</span></span>
<span data-ttu-id="84c15-113">Kullanıcının adres defterinde görüntülenecek yeni ad.</span><span class="sxs-lookup"><span data-stu-id="84c15-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="84c15-114">Örnek-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="84c15-114">Example-'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c15-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="84c15-115">-EnableAccount</span></span>
<span data-ttu-id="84c15-116">Hesabı etkinleştirmek için doğru; Aksi takdirde, false.</span><span class="sxs-lookup"><span data-stu-id="84c15-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c15-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="84c15-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="84c15-118">Yalnızca parolayı güncelleştirirken belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="84c15-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="84c15-119">Aksi takdirde yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="84c15-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="84c15-120">Kullanıcının sonraki başarılı oturum açmada parolasını değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="84c15-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="84c15-121">Sonraki başarılı oturum açmada parola değişimi için varsayılan davranış (false) olur.</span><span class="sxs-lookup"><span data-stu-id="84c15-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c15-122">-Parola</span><span class="sxs-lookup"><span data-stu-id="84c15-122">-Password</span></span>
<span data-ttu-id="84c15-123">Kullanıcı için yeni parola.</span><span class="sxs-lookup"><span data-stu-id="84c15-123">New password for the user.</span></span>
<span data-ttu-id="84c15-124">Kiracının parola karmaşıklığı gereksinimlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="84c15-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="84c15-125">Güçlü bir parola ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="84c15-125">It is recommended to set a strong password.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c15-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="84c15-126">-UPNOrObjectId</span></span>
<span data-ttu-id="84c15-127">Kullanıcı asıl adı (örneğin, ' someuser@contoso.com ') veya özelliklerin güncellenmesi gereken kullanıcının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="84c15-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c15-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="84c15-128">-Confirm</span></span>
<span data-ttu-id="84c15-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84c15-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c15-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c15-130">-WhatIf</span></span>
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

### <span data-ttu-id="84c15-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c15-131">-DefaultProfile</span></span>
<span data-ttu-id="84c15-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84c15-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c15-133">CommonParameters</span></span>
<span data-ttu-id="84c15-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84c15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c15-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c15-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c15-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84c15-136">INPUTS</span></span>

## <span data-ttu-id="84c15-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84c15-137">OUTPUTS</span></span>

### <span data-ttu-id="84c15-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="84c15-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="84c15-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84c15-139">NOTES</span></span>

## <span data-ttu-id="84c15-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84c15-140">RELATED LINKS</span></span>

[<span data-ttu-id="84c15-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="84c15-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="84c15-142">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="84c15-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="84c15-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="84c15-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

