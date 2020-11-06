---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593442"
---
# <span data-ttu-id="5cc4b-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5cc4b-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="5cc4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc4b-103">Hizmet sorumlusunun kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cc4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-104">SYNTAX</span></span>

### <span data-ttu-id="5cc4b-105">NesneKimliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cc4b-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-106">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="5cc4b-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cc4b-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cc4b-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc4b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cc4b-109">DESCRIPTION</span></span>
<span data-ttu-id="5cc4b-110">Remove-AzureRmADSpCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir hizmet sorumlusunun kimlik bilgilerini kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="5cc4b-111">Hizmet sorumlusu, nesne KIMLIĞI veya hizmet asıl adı (SPN) sunarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="5cc4b-112">Kaldırılacak kimlik bilgileri, tek bir kimlik bilgisinin kaldırılması veya bir ' tümü ' anahtarıyla, hizmet sorumlusu ile ilişkili tüm kimlik bilgilerinin silinmesi durumunda, bu kişinin anahtar KIMLIĞI tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="5cc4b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cc4b-113">EXAMPLES</span></span>

### <span data-ttu-id="5cc4b-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cc4b-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="5cc4b-115">Bu komut, hizmet sorumlusunun kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="5cc4b-116">Bu örnekte, "9044423a-60a3-45ac-9ab1-09534157ebb" kimliğine sahip anahtar hizmet sorumlusunun kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="5cc4b-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5cc4b-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="5cc4b-118">Bu komut, hizmet sorumlusunun kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="5cc4b-119">Bu örnekte, tüm kimlik bilgileri, hizmet asıl adı "" ile ilişkilendirilmiş hizmet sorumlusunun altında kaldırılacaktır http://test123 .</span><span class="sxs-lookup"><span data-stu-id="5cc4b-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="5cc4b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cc4b-120">PARAMETERS</span></span>

### <span data-ttu-id="5cc4b-121">-Tümü</span><span class="sxs-lookup"><span data-stu-id="5cc4b-121">-All</span></span>
<span data-ttu-id="5cc4b-122">Hizmet sorumlusu ile ilişkili tüm kimlik bilgilerini kaldırmak için geçiş yapın.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc4b-123">-DefaultProfile</span></span>
<span data-ttu-id="5cc4b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cc4b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cc4b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5cc4b-125">-Force</span></span>
<span data-ttu-id="5cc4b-126">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc4b-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5cc4b-127">-KeyId</span></span>
<span data-ttu-id="5cc4b-128">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="5cc4b-129">Hizmet sorumlusunun anahtar kimlikleri Get-AzureRmADSpCredential cmdlet kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc4b-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5cc4b-130">-ObjectId</span></span>
<span data-ttu-id="5cc4b-131">Kimlik bilgilerini kaldırmak için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc4b-132">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5cc4b-132">-ServicePrincipalName</span></span>
<span data-ttu-id="5cc4b-133">Kimlik bilgilerinin kaldırılacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="5cc4b-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc4b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cc4b-134">-Confirm</span></span>
<span data-ttu-id="5cc4b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc4b-136">-WhatIf</span></span>
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

### <span data-ttu-id="5cc4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc4b-137">CommonParameters</span></span>
<span data-ttu-id="5cc4b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc4b-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc4b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc4b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-140">INPUTS</span></span>

### <span data-ttu-id="5cc4b-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5cc4b-141">None</span></span>
<span data-ttu-id="5cc4b-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5cc4b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cc4b-143">OUTPUTS</span></span>

## <span data-ttu-id="5cc4b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cc4b-144">NOTES</span></span>

## <span data-ttu-id="5cc4b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cc4b-145">RELATED LINKS</span></span>

[<span data-ttu-id="5cc4b-146">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5cc4b-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="5cc4b-147">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5cc4b-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="5cc4b-148">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5cc4b-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

