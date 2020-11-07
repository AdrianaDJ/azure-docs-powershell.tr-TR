---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: 342ab551afdce144719d5ba49c25eb7559ba35a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761954"
---
# <span data-ttu-id="4d855-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4d855-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="4d855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d855-102">SYNOPSIS</span></span>
<span data-ttu-id="4d855-103">Hizmet sorumlusunun kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d855-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d855-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d855-104">SYNTAX</span></span>

### <span data-ttu-id="4d855-105">NesneKimliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d855-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d855-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d855-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d855-107">Displaynamewithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4d855-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d855-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d855-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d855-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d855-109">DESCRIPTION</span></span>
<span data-ttu-id="4d855-110">Remove-AzureRmADSpCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir hizmet sorumlusunun kimlik bilgilerini kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4d855-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="4d855-111">Hizmet sorumlusu, nesne KIMLIĞI veya hizmet asıl adı (SPN) sunarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4d855-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="4d855-112">Kaldırılacak kimlik bilgileri, tek bir kimlik bilgisinin kaldırılması veya bir ' tümü ' anahtarıyla, hizmet sorumlusu ile ilişkili tüm kimlik bilgilerinin silinmesi durumunda, bu kişinin anahtar KIMLIĞI tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4d855-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="4d855-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d855-113">EXAMPLES</span></span>

### <span data-ttu-id="4d855-114">Örnek 1-hizmet sorumlusunun belirli kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d855-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="4d855-115">Anahtar kimliği ' 9044423a-60a3-45ac-9ab1-09534157ebb ' olan kimlik bilgisini nesne kimliği ' 7663d3fb-6f86-4352-9e613-cf9vseç50)5ee82 ' ile birlikte kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d855-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="4d855-116">Örnek 2-hizmet sorumlusunun tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d855-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="4d855-117">Hizmet sorumlusunun tüm kimlik bilgilerini SPN "" ile kaldırır http://test123 .</span><span class="sxs-lookup"><span data-stu-id="4d855-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="4d855-118">Örnek 3-boru kullanarak hizmet sorumlusunun tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d855-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="4d855-119">' 7663d3fb-6f86-4352-9e613-cf9vseç50)'in bu hizmet sorumlusunun tüm kimlik bilgilerini kaldırmasını için Remove-AzureRmADSpCredential cmdlet 'ine sahip hizmet sorumlusunu alır.</span><span class="sxs-lookup"><span data-stu-id="4d855-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="4d855-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d855-120">PARAMETERS</span></span>

### <span data-ttu-id="4d855-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d855-121">-DefaultProfile</span></span>
<span data-ttu-id="4d855-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4d855-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d855-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4d855-123">-DisplayName</span></span>
<span data-ttu-id="4d855-124">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="4d855-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="4d855-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4d855-125">-Force</span></span>
<span data-ttu-id="4d855-126">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="4d855-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="4d855-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4d855-127">-KeyId</span></span>
<span data-ttu-id="4d855-128">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d855-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="4d855-129">Hizmet sorumlusunun anahtar kimlikleri Get-AzureRmADSpCredential cmdlet kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d855-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="4d855-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4d855-130">-ObjectId</span></span>
<span data-ttu-id="4d855-131">Kimlik bilgilerini kaldırmak için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="4d855-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d855-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4d855-132">-PassThru</span></span>
<span data-ttu-id="4d855-133">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="4d855-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4d855-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4d855-134">-ServicePrincipalName</span></span>
<span data-ttu-id="4d855-135">Kimlik bilgilerinin kaldırılacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="4d855-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="4d855-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="4d855-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="4d855-137">Kimlik bilgilerini kaldırmak için hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4d855-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d855-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d855-138">-Confirm</span></span>
<span data-ttu-id="4d855-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d855-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d855-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d855-140">-WhatIf</span></span>
<span data-ttu-id="4d855-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d855-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d855-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d855-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d855-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d855-143">CommonParameters</span></span>
<span data-ttu-id="4d855-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d855-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d855-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d855-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d855-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d855-146">INPUTS</span></span>

### <span data-ttu-id="4d855-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="4d855-147">System.Guid</span></span>

### <span data-ttu-id="4d855-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4d855-148">System.String</span></span>

### <span data-ttu-id="4d855-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4d855-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="4d855-150">Parametreler: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d855-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="4d855-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d855-151">OUTPUTS</span></span>

### <span data-ttu-id="4d855-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d855-152">System.Boolean</span></span>

## <span data-ttu-id="4d855-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d855-153">NOTES</span></span>

## <span data-ttu-id="4d855-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d855-154">RELATED LINKS</span></span>

[<span data-ttu-id="4d855-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4d855-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="4d855-156">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4d855-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="4d855-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4d855-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

