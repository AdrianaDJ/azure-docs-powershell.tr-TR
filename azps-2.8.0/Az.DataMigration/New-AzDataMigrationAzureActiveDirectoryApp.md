---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752260"
---
# <span data-ttu-id="f3006-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f3006-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f3006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3006-102">SYNOPSIS</span></span>
<span data-ttu-id="f3006-103">Yeni bir örnek oluştur DataMigration Azure ActiveDirectory uygulaması ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="f3006-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f3006-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3006-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3006-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3006-105">DESCRIPTION</span></span>
<span data-ttu-id="f3006-106">Yeni bir örnek oluştur DataMigration Azure ActiveDirectory uygulaması ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="f3006-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f3006-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3006-107">EXAMPLES</span></span>

### <span data-ttu-id="f3006-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3006-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="f3006-109">ApplicationId: "AppID/hizmet asıl kimliği burada" AppKey: System. Security. SecureString Tenantıd: "Kiracı kimliği"</span><span class="sxs-lookup"><span data-stu-id="f3006-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="f3006-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3006-110">PARAMETERS</span></span>

### <span data-ttu-id="f3006-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="f3006-111">-AppKey</span></span>
<span data-ttu-id="f3006-112">Azure Active Directory anahtarı</span><span class="sxs-lookup"><span data-stu-id="f3006-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3006-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f3006-113">-ApplicationId</span></span>
<span data-ttu-id="f3006-114">Azure Active Directory Uygulama kimliği</span><span class="sxs-lookup"><span data-stu-id="f3006-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3006-115">-DefaultProfile</span></span>
<span data-ttu-id="f3006-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3006-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3006-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3006-117">CommonParameters</span></span>
<span data-ttu-id="f3006-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3006-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3006-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3006-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3006-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3006-120">INPUTS</span></span>

### <span data-ttu-id="f3006-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f3006-121">None</span></span>

## <span data-ttu-id="f3006-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3006-122">OUTPUTS</span></span>

### <span data-ttu-id="f3006-123">Microsoft. Azure. Commands. DataMigration. modeller. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f3006-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f3006-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3006-124">NOTES</span></span>

## <span data-ttu-id="f3006-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3006-125">RELATED LINKS</span></span>
