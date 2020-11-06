---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588369"
---
# <span data-ttu-id="668dd-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668dd-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="668dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668dd-102">SYNOPSIS</span></span>
<span data-ttu-id="668dd-103">Uygulamadaki kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="668dd-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="668dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="668dd-104">SYNTAX</span></span>

### <span data-ttu-id="668dd-105">Applicationobjectivseçwithkeyidparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="668dd-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668dd-106">Applicationıdwithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="668dd-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668dd-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="668dd-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668dd-108">Applicationobjectwithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="668dd-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668dd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="668dd-109">DESCRIPTION</span></span>
<span data-ttu-id="668dd-110">Remove-AzureRmADAppCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir uygulamadan kimlik bilgileri kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="668dd-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="668dd-111">Uygulama, nesne KIMLIĞI veya AppID sağlayarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="668dd-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="668dd-112">Kaldırılacak kimlik bilgileri, anahtar KIMLIĞIYLE tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="668dd-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="668dd-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="668dd-113">EXAMPLES</span></span>

### <span data-ttu-id="668dd-114">Örnek 1-uygulamadan belirli bir kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="668dd-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="668dd-115">Anahtar kimliği ' 9044423a-60a3-45ac-9ab1-09534157ebb ' olan kimlik bilgisini uygulamadan nesne kimliği ' 7663d3fb-6f86-4352-9e6vseç-cf9vseç50vseç5ee82 ' ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="668dd-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="668dd-116">Örnek 2-uygulamadaki tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="668dd-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="668dd-117">Uygulamadaki tüm kimlik bilgilerini ' 4589cd6b-3d79-4bb4-93b8-a0bfc58 ' uygulama kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="668dd-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="668dd-118">Örnek 3-boru kullanarak tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="668dd-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="668dd-119">Uygulama kimliği ' 7663d3fb-6f86-4352-9e613-cf9vseç50vseç5ee82 ' ve Remove-AzureRmADAppCredential kanallar ile bu uygulamadaki tüm kimlik bilgilerini kaldıran uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="668dd-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="668dd-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="668dd-120">PARAMETERS</span></span>

### <span data-ttu-id="668dd-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="668dd-121">-ApplicationId</span></span>
<span data-ttu-id="668dd-122">Kimlik bilgilerinin kaldırılacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="668dd-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668dd-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="668dd-123">-ApplicationObject</span></span>
<span data-ttu-id="668dd-124">Kimlik bilgilerini kaldırmak için uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="668dd-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="668dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668dd-125">-DefaultProfile</span></span>
<span data-ttu-id="668dd-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="668dd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="668dd-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="668dd-127">-DisplayName</span></span>
<span data-ttu-id="668dd-128">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="668dd-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668dd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="668dd-129">-Force</span></span>
<span data-ttu-id="668dd-130">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="668dd-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="668dd-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="668dd-131">-KeyId</span></span>
<span data-ttu-id="668dd-132">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="668dd-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="668dd-133">Uygulamanın anahtar kimlikleri, Get-AzureRmADAppCredential cmdlet 'i kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="668dd-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668dd-134">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="668dd-134">-ObjectId</span></span>
<span data-ttu-id="668dd-135">Kimlik bilgilerinin kaldırılacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="668dd-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668dd-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="668dd-136">-PassThru</span></span>
<span data-ttu-id="668dd-137">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="668dd-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="668dd-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="668dd-138">-Confirm</span></span>
<span data-ttu-id="668dd-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="668dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668dd-140">-WhatIf</span></span>
<span data-ttu-id="668dd-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="668dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668dd-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="668dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668dd-143">CommonParameters</span></span>
<span data-ttu-id="668dd-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="668dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668dd-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668dd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668dd-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="668dd-146">INPUTS</span></span>

### <span data-ttu-id="668dd-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="668dd-147">System.Guid</span></span>

### <span data-ttu-id="668dd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="668dd-148">System.String</span></span>

### <span data-ttu-id="668dd-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="668dd-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="668dd-150">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="668dd-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="668dd-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="668dd-151">OUTPUTS</span></span>

### <span data-ttu-id="668dd-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="668dd-152">System.Boolean</span></span>

## <span data-ttu-id="668dd-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="668dd-153">NOTES</span></span>

## <span data-ttu-id="668dd-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="668dd-154">RELATED LINKS</span></span>

[<span data-ttu-id="668dd-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668dd-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="668dd-156">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668dd-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="668dd-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="668dd-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
