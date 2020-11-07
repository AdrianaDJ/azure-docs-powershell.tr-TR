---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 8a034bc85209e0325547bac2f64f277ceaee0abc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933760"
---
# <span data-ttu-id="af177-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="af177-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="af177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af177-102">SYNOPSIS</span></span>
<span data-ttu-id="af177-103">SQL yönetilen örneği için bir Azure AD yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="af177-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="af177-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af177-104">SYNTAX</span></span>

### <span data-ttu-id="af177-105">Useresourcegroupandınstancenameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af177-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af177-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af177-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af177-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="af177-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af177-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af177-108">DESCRIPTION</span></span>
<span data-ttu-id="af177-109">**Set-Azsqlınstanceactivedirectoryadministrator** cmdlet 'i, geçerli abonelikte AzureSQL yönetilen örneği Için bir Azure Active Directory (Azure AD) Yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="af177-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="af177-110">Aynı anda yalnızca bir yönetici temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af177-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="af177-111">Aşağıdaki Azure AD üyeleri SQL yönetilen örnek Yöneticisi olarak sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="af177-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="af177-112">Yerel Azure AD üyeleri</span><span class="sxs-lookup"><span data-stu-id="af177-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="af177-113">Şirket içindeki Federasyon üyeleri</span><span class="sxs-lookup"><span data-stu-id="af177-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="af177-114">Başka Azure reklamlardan alınan güvenlik grupları tarafından oluşturulan Azure AD grupları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="af177-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="af177-115">Outlook.com, Hotmail.com veya Live.com etki alanlarında olduğu gibi Microsoft hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="af177-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="af177-116">Gmail.com veya Yahoo.com etki alanlarında olduğu gibi diğer Konuk hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="af177-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="af177-117">Adanmış bir Azure AD grubunu yönetici olarak sağlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="af177-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="af177-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af177-118">EXAMPLES</span></span>

### <span data-ttu-id="af177-119">Örnek 1: kaynak grubuyla ilişkilendirilmiş yönetilen bir örnek için yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="af177-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="af177-120">Bu komut, ManagedInstance01 adlı yönetilen örnek için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="af177-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="af177-121">Bu sunucu, kaynak grubu ResourceGroup01 ile ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="af177-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="af177-122">Örnek 2: yönetilen örnek nesnesini kullanarak Yönetici Kullanıcı hazırlama</span><span class="sxs-lookup"><span data-stu-id="af177-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="af177-123">Bu komut, yönetilen örnek nesnesinden bir Azure AD kullanıcısını yönetici olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="af177-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="af177-124">Örnek 3: yönetilen örnek kaynak tanımlayıcısını kullanarak yönetici hazırlama</span><span class="sxs-lookup"><span data-stu-id="af177-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="af177-125">Bu komut, yönetilen örnek kaynak tanımlayıcısını kullanan bir Azure AD kullanıcısını yönetici olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="af177-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="af177-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af177-126">PARAMETERS</span></span>

### <span data-ttu-id="af177-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af177-127">-DefaultProfile</span></span>
<span data-ttu-id="af177-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af177-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af177-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="af177-129">-DisplayName</span></span>
<span data-ttu-id="af177-130">İzin verilecek kullanıcının veya grubun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af177-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="af177-131">Bu görünen ad, geçerli abonelikle ilişkilendirilmiş Active Directory 'de bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af177-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af177-132">-InputObject</span></span>
<span data-ttu-id="af177-133">Kullanılacak yönetilen örnek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="af177-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="af177-134">-InstanceName</span></span>
<span data-ttu-id="af177-135">SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="af177-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="af177-136">-ObjectId</span></span>
<span data-ttu-id="af177-137">İzin verilecek Azure Active Directory 'de kullanıcının veya grubun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="af177-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af177-138">-ResourceGroupName</span></span>
<span data-ttu-id="af177-139">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="af177-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="af177-140">-ResourceId</span></span>
<span data-ttu-id="af177-141">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="af177-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af177-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="af177-142">-Confirm</span></span>
<span data-ttu-id="af177-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af177-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af177-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af177-144">-WhatIf</span></span>
<span data-ttu-id="af177-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af177-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af177-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af177-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af177-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af177-147">CommonParameters</span></span>
<span data-ttu-id="af177-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af177-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af177-149">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af177-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af177-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af177-150">INPUTS</span></span>

### <span data-ttu-id="af177-151">System. String</span><span class="sxs-lookup"><span data-stu-id="af177-151">System.String</span></span>

### <span data-ttu-id="af177-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="af177-152">System.Guid</span></span>

## <span data-ttu-id="af177-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af177-153">OUTPUTS</span></span>

### <span data-ttu-id="af177-154">Microsoft. Azure. Commands. Sql. ınstanceactivedirectoryadministrator. model. Azuresdınstanceactivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="af177-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="af177-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af177-155">NOTES</span></span>

## <span data-ttu-id="af177-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af177-156">RELATED LINKS</span></span>

[<span data-ttu-id="af177-157">Get-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="af177-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="af177-158">Remove-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="af177-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
