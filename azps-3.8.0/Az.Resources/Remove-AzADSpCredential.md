---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 669a1beecaed14c0ab0705979188995daaf9d95f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937647"
---
# <span data-ttu-id="706d5-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="706d5-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="706d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706d5-102">SYNOPSIS</span></span>
<span data-ttu-id="706d5-103">Hizmet sorumlusunun kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="706d5-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="706d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="706d5-104">SYNTAX</span></span>

### <span data-ttu-id="706d5-105">NesneKimliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="706d5-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="706d5-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="706d5-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="706d5-107">Displaynamewithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="706d5-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="706d5-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="706d5-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="706d5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="706d5-109">DESCRIPTION</span></span>
<span data-ttu-id="706d5-110">Remove-AzADSpCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir hizmet sorumlusunun kimlik bilgilerini kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="706d5-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="706d5-111">Hizmet sorumlusu, nesne KIMLIĞI veya hizmet asıl adı (SPN) sunarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="706d5-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="706d5-112">Kaldırılacak kimlik bilgileri, tek bir kimlik bilgisinin kaldırılması veya bir ' tümü ' anahtarıyla, hizmet sorumlusu ile ilişkili tüm kimlik bilgilerinin silinmesi durumunda, bu kişinin anahtar KIMLIĞI tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="706d5-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="706d5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="706d5-113">EXAMPLES</span></span>

### <span data-ttu-id="706d5-114">Örnek 1-hizmet sorumlusunun belirli kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="706d5-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="706d5-115">Anahtar kimliği ' 9044423a-60a3-45ac-9ab1-09534157ebb ' olan kimlik bilgisini nesne kimliği ' 7663d3fb-6f86-4352-9e613-cf9vseç50)5ee82 ' ile birlikte kaldırır.</span><span class="sxs-lookup"><span data-stu-id="706d5-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="706d5-116">Örnek 2-hizmet sorumlusunun tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="706d5-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="706d5-117">Hizmet sorumlusunun tüm kimlik bilgilerini SPN "" ile kaldırır http://test123 .</span><span class="sxs-lookup"><span data-stu-id="706d5-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="706d5-118">Örnek 3-boru kullanarak hizmet sorumlusunun tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="706d5-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="706d5-119">' 7663d3fb-6f86-4352-9e613-cf9vseç50)'in bu hizmet sorumlusunun tüm kimlik bilgilerini kaldırmasını için Remove-AzADSpCredential cmdlet 'ine sahip hizmet sorumlusunu alır.</span><span class="sxs-lookup"><span data-stu-id="706d5-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="706d5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="706d5-120">PARAMETERS</span></span>

### <span data-ttu-id="706d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706d5-121">-DefaultProfile</span></span>
<span data-ttu-id="706d5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="706d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="706d5-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="706d5-123">-DisplayName</span></span>
<span data-ttu-id="706d5-124">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="706d5-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="706d5-125">-Force</span></span>
<span data-ttu-id="706d5-126">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="706d5-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="706d5-127">-KeyId</span></span>
<span data-ttu-id="706d5-128">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="706d5-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="706d5-129">Hizmet sorumlusunun anahtar kimlikleri Get-AzADSpCredential cmdlet kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="706d5-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="706d5-130">-ObjectId</span></span>
<span data-ttu-id="706d5-131">Kimlik bilgilerini kaldırmak için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="706d5-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="706d5-132">-PassThru</span></span>
<span data-ttu-id="706d5-133">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="706d5-133">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="706d5-134">-ServicePrincipalName</span></span>
<span data-ttu-id="706d5-135">Kimlik bilgilerinin kaldırılacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="706d5-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="706d5-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="706d5-137">Kimlik bilgilerini kaldırmak için hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="706d5-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="706d5-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="706d5-138">-Confirm</span></span>
<span data-ttu-id="706d5-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="706d5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="706d5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706d5-140">-WhatIf</span></span>
<span data-ttu-id="706d5-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="706d5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="706d5-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="706d5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="706d5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706d5-143">CommonParameters</span></span>
<span data-ttu-id="706d5-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="706d5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706d5-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="706d5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706d5-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="706d5-146">INPUTS</span></span>

### <span data-ttu-id="706d5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="706d5-147">System.String</span></span>

### <span data-ttu-id="706d5-148">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="706d5-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="706d5-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="706d5-149">System.Guid</span></span>

## <span data-ttu-id="706d5-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="706d5-150">OUTPUTS</span></span>

### <span data-ttu-id="706d5-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="706d5-151">System.Boolean</span></span>

## <span data-ttu-id="706d5-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="706d5-152">NOTES</span></span>

## <span data-ttu-id="706d5-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="706d5-153">RELATED LINKS</span></span>

[<span data-ttu-id="706d5-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="706d5-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="706d5-155">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="706d5-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="706d5-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="706d5-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

