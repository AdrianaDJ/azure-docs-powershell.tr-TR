---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 5c47e707c3421c6efc1998e55897f6bb9be8fa65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759363"
---
# <span data-ttu-id="50c3d-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50c3d-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="50c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="50c3d-103">Uygulamadaki kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="50c3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50c3d-104">SYNTAX</span></span>

### <span data-ttu-id="50c3d-105">Applicationobjectivseçwithkeyidparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50c3d-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c3d-106">Applicationıdwithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="50c3d-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c3d-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50c3d-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c3d-108">Applicationobjectwithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="50c3d-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c3d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="50c3d-109">DESCRIPTION</span></span>
<span data-ttu-id="50c3d-110">Remove-AzADAppCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir uygulamadan kimlik bilgileri kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="50c3d-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="50c3d-111">Uygulama, nesne KIMLIĞI veya AppID sağlayarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="50c3d-112">Kaldırılacak kimlik bilgileri, anahtar KIMLIĞIYLE tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="50c3d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50c3d-113">EXAMPLES</span></span>

### <span data-ttu-id="50c3d-114">Örnek 1-uygulamadan belirli bir kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="50c3d-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="50c3d-115">Anahtar kimliği ' 9044423a-60a3-45ac-9ab1-09534157ebb ' olan kimlik bilgisini uygulamadan nesne kimliği ' 7663d3fb-6f86-4352-9e6vseç-cf9vseç50vseç5ee82 ' ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="50c3d-116">Örnek 2-uygulamadaki tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="50c3d-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="50c3d-117">Uygulamadaki tüm kimlik bilgilerini ' 4589cd6b-3d79-4bb4-93b8-a0bfc58 ' uygulama kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="50c3d-118">Örnek 3-boru kullanarak tüm kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="50c3d-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="50c3d-119">Uygulama kimliği ' 7663d3fb-6f86-4352-9e613-cf9vseç50vseç5ee82 ' ve Remove-AzADAppCredential kanallar ile bu uygulamadaki tüm kimlik bilgilerini kaldıran uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="50c3d-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="50c3d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50c3d-120">PARAMETERS</span></span>

### <span data-ttu-id="50c3d-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50c3d-121">-ApplicationId</span></span>
<span data-ttu-id="50c3d-122">Kimlik bilgilerinin kaldırılacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="50c3d-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="50c3d-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="50c3d-123">-ApplicationObject</span></span>
<span data-ttu-id="50c3d-124">Kimlik bilgilerini kaldırmak için uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="50c3d-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50c3d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c3d-125">-DefaultProfile</span></span>
<span data-ttu-id="50c3d-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50c3d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50c3d-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50c3d-127">-DisplayName</span></span>
<span data-ttu-id="50c3d-128">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="50c3d-128">The display name of the application.</span></span>

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

### <span data-ttu-id="50c3d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="50c3d-129">-Force</span></span>
<span data-ttu-id="50c3d-130">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="50c3d-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="50c3d-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="50c3d-131">-KeyId</span></span>
<span data-ttu-id="50c3d-132">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50c3d-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="50c3d-133">Uygulamanın anahtar kimlikleri, Get-AzADAppCredential cmdlet 'i kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="50c3d-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="50c3d-134">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="50c3d-134">-ObjectId</span></span>
<span data-ttu-id="50c3d-135">Kimlik bilgilerinin kaldırılacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="50c3d-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c3d-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="50c3d-136">-PassThru</span></span>
<span data-ttu-id="50c3d-137">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="50c3d-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="50c3d-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="50c3d-138">-Confirm</span></span>
<span data-ttu-id="50c3d-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50c3d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c3d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c3d-140">-WhatIf</span></span>
<span data-ttu-id="50c3d-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50c3d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50c3d-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50c3d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c3d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c3d-143">CommonParameters</span></span>
<span data-ttu-id="50c3d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50c3d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c3d-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c3d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c3d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50c3d-146">INPUTS</span></span>

### <span data-ttu-id="50c3d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="50c3d-147">System.String</span></span>

### <span data-ttu-id="50c3d-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="50c3d-148">System.Guid</span></span>

### <span data-ttu-id="50c3d-149">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="50c3d-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="50c3d-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50c3d-150">OUTPUTS</span></span>

### <span data-ttu-id="50c3d-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50c3d-151">System.Boolean</span></span>

## <span data-ttu-id="50c3d-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50c3d-152">NOTES</span></span>

## <span data-ttu-id="50c3d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50c3d-153">RELATED LINKS</span></span>

[<span data-ttu-id="50c3d-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50c3d-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="50c3d-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50c3d-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="50c3d-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="50c3d-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)