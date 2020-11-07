---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: f5cd00e0ef8e8936a4c87ee313054ae4c084a879
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93940243"
---
# <span data-ttu-id="d9186-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9186-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="d9186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9186-102">SYNOPSIS</span></span>
<span data-ttu-id="d9186-103">Bir kullanıcı veya uygulamadaki tüm izinleri anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="d9186-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9186-104">SYNTAX</span></span>

### <span data-ttu-id="d9186-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9186-105">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9186-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9186-106">ByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9186-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="d9186-107">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9186-108">Elektronik posta</span><span class="sxs-lookup"><span data-stu-id="d9186-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9186-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="d9186-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9186-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9186-110">DESCRIPTION</span></span>
<span data-ttu-id="d9186-111">**Remove-Azanahtar,** bir kullanıcı veya uygulamadaki tüm izinleri veya anahtar kasasından tüm kullanıcıları ve uygulamaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-111">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="d9186-112">Tüm izinleri kaldırsanız bile, anahtar kasası içeren Azure aboneliğinin sahibi anahtar kasasına izinler ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="d9186-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="d9186-113">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d9186-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="d9186-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9186-114">EXAMPLES</span></span>

### <span data-ttu-id="d9186-115">Örnek 1: kullanıcının izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d9186-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="d9186-116">Bu komut, kullanıcının PattiFuller@contoso.com Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="d9186-117">Örnek 2: bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d9186-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="d9186-118">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="d9186-119">Bu örnek, Azure Active Directory 'de kaydedilen hizmet asıl adını kullanarak uygulamayı tanımlar `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="d9186-119">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="d9186-120">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d9186-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="d9186-121">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="d9186-122">Bu örnekte uygulama, hizmet sorumlusunun nesne KIMLIĞINE göre tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d9186-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="d9186-123">Örnek 4: Microsoft. COMPUTE kaynak sağlayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d9186-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="d9186-124">Bu komut, Microsoft. COMPUTE Resource Provider 'ın Contoso03Vault 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="d9186-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9186-125">PARAMETERS</span></span>

### <span data-ttu-id="d9186-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d9186-126">-ApplicationId</span></span>
<span data-ttu-id="d9186-127">.</span><span class="sxs-lookup"><span data-stu-id="d9186-127">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9186-128">-DefaultProfile</span></span>
<span data-ttu-id="d9186-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9186-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-130">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="d9186-130">-EmailAddress</span></span>
<span data-ttu-id="d9186-131">Erişimini kaldırmak istediğiniz kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d9186-132">-EnabledForDeployment</span></span>
<span data-ttu-id="d9186-133">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9186-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d9186-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d9186-135">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="d9186-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d9186-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d9186-137">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="d9186-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-138">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="d9186-138">-ObjectId</span></span>
<span data-ttu-id="d9186-139">İzinleri kaldırmak için Azure Active Directory 'de Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d9186-140">-PassThru</span></span>
<span data-ttu-id="d9186-141">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9186-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9186-142">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d9186-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9186-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9186-143">-ResourceGroupName</span></span>
<span data-ttu-id="d9186-144">Erişim ilkesi değiştirildikleri Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="d9186-145">Belirtilmemişse, bu cmdlet geçerli abonelikte Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="d9186-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9186-146">-ServicePrincipalName</span></span>
<span data-ttu-id="d9186-147">İzinlerini kaldırmak istediğiniz uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="d9186-148">Azure Active Directory 'de uygulama için kaydettirilmiş olan uygulama KIMLIĞI 'ni belirtin.</span><span class="sxs-lookup"><span data-stu-id="d9186-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9186-149">-UserPrincipalName</span></span>
<span data-ttu-id="d9186-150">Erişimini kaldırmak istediğiniz kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d9186-151">-VaultName</span></span>
<span data-ttu-id="d9186-152">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9186-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="d9186-153">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası izinlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9186-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9186-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9186-154">-Confirm</span></span>
<span data-ttu-id="d9186-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9186-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9186-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9186-156">-WhatIf</span></span>
<span data-ttu-id="d9186-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9186-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9186-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9186-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9186-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9186-159">CommonParameters</span></span>
<span data-ttu-id="d9186-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9186-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9186-161">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9186-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9186-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9186-162">INPUTS</span></span>

### <span data-ttu-id="d9186-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d9186-163">None</span></span>
<span data-ttu-id="d9186-164">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d9186-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9186-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9186-165">OUTPUTS</span></span>

### <span data-ttu-id="d9186-166">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="d9186-166">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="d9186-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9186-167">NOTES</span></span>

## <span data-ttu-id="d9186-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9186-168">RELATED LINKS</span></span>

[<span data-ttu-id="d9186-169">Set-Azanahtarvaultaccesspolicy</span><span class="sxs-lookup"><span data-stu-id="d9186-169">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

